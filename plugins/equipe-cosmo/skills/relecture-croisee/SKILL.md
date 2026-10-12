---
name: relecture-croisee
description: Relecture indépendante et critique d'un livrable produit par un autre agent (contrat, devis, e-mail externe, business plan, analyse fiscale, plan) sous plusieurs angles - exactitude, chiffres, juridique, forme, cohérence avec les décisions - avec verdict OK / OK avec réserves / À REPRENDRE. À utiliser avant toute demande de validation à Corentin.
---

# Relecture croisée

Inspiré de `cross-eval` (alirezarezvani/claude-skills, MIT) et `multi-reviewer-patterns` (wshobson/agents, MIT). Réécrit, sans appel à d'autres modèles.

**Posture** : supposer que le livrable contient des erreurs jusqu'à preuve du contraire. Ne pas être complaisant.

## Angles (appliquer ceux qui concernent le livrable)
1. **Exactitude** : chaque fait et chiffre est-il sourcé ? Les taux légaux ont-ils une source officielle datée ?
2. **Calculs** : refaire les totaux, TVA, pourcentages, échéanciers.
3. **Juridique** : mentions obligatoires, engagements pris au nom de Corentin, risques non signalés.
4. **Cohérence** : avec les fiches entités et le journal des décisions (contradiction = 🔴).
5. **Destinataire** : un lecteur extérieur comprend-il ? ton adapté ? fautes ? bonne entité émettrice ?
6. **Sécurité** : données personnelles inutiles, pièce jointe sensible, destinataire correct.

## Sortie
```
Verdict : 🟢 OK | 🟡 OK avec réserves | 🔴 À REPRENDRE
Problèmes bloquants : …
Réserves : …
Vérifications faites : … (avec preuves)
```
Un 🔴 renvoie le livrable à l'agent auteur ; il ne va pas à Corentin. Le verdict est recopié dans la file de validation.
