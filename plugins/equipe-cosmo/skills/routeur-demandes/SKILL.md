---
name: routeur-demandes
description: Porte d'entrée de l'équipe. Comprend une demande de Corentin, même floue ou orale (« il faudrait qu'on… », « je sais pas par où commencer »), identifie l'entité concernée et l'agent ou le skill le plus adapté, puis lance le travail. À utiliser pour toute demande ouverte qui ne correspond pas clairement à un seul skill.
---

# Routeur de demandes

Inspiré de `smb-router` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

## Étapes

1. **Reformuler** en une phrase ce que Corentin veut obtenir (le résultat, pas la tâche).
2. **Identifier l'entité** : micro-entreprise, SAS, holding, immobilier, Créaxia, Crenovia, école, ou « transverse ».
   Si ambigu, poser **une seule** question.
3. **Lire le contexte** : la fiche `bureau/entites/<entité>.md` et les décisions actives liées dans `bureau/decisions/journal.md`.
4. **Choisir qui fait quoi** :

| Signal dans la demande | Agent |
|---|---|
| idée nouvelle, choix, stratégie, marché, business plan | `directeur-strategie` (+ skill `affiner-idee` si l'idée est brute) |
| contrat, statuts, société, obligation légale, litige | `juriste` |
| argent, facture, trésorerie, impôts, URSSAF, TVA, investissement | `directeur-financier` |
| outil, site, logiciel, automatisation, données, sécurité | `directeur-technique` |
| visite, diagnostic, chiffrage travaux, CCTP, DCE, devis d'entreprises à comparer (mission AMO) | `ingenieur-amo` |
| client, prospect, devis, e-mail, réseaux, avis | `responsable-commercial` |
| cours, rendu, examen, mémoire | `assistant-ecole` |

   Sujet multi-domaines (ex. passage micro → SAS = juriste + financier + stratégie) : lancer les agents **en parallèle**
   avec chacun un brief précis, puis faire la synthèse.
5. **Niveau de complexité** (1 simple / 2 standard / 3 complexe, voir CLAUDE.md « Économie ») → choisir `model` et
   `effort` de l'appel Agent en conséquence.
6. **Brief compact à l'agent** (10 lignes max) : objectif, entité, chemins des fichiers à lire (pas leur contenu),
   livrable attendu, contraintes (délai, budget), rappel « brouillon uniquement, rien n'est envoyé ».
7. **Après le retour** : relecture par `controleur-qualite` si le livrable part vers l'extérieur, engage de l'argent
   ou une décision juridique ; puis entrée dans la file (`file-validation`) si une action sortante est nécessaire.
8. **Répondre à Corentin** : 3-6 lignes — ce qui a été fait, ce qui attend sa validation (avec ID), prochaine étape.

## À éviter
- Poser plusieurs questions d'un coup. Proposer une hypothèse par défaut et avancer.
- Faire soi-même un travail d'expert alors qu'un agent existe.
