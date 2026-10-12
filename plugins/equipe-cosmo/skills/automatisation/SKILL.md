---
name: automatisation
description: Met en place et fait tourner l'automatisation de l'équipe - propose les tâches planifiées (point du jour, tri des mails, prospection CRENOVIA, suivi des réponses, point hebdo, clôture mensuelle) et fait exécuter le travail répétitif par des agents économes (Haiku) quel que soit le modèle de la session. À utiliser quand Corentin demande d'automatiser, à la fin du premier lancement du bureau, ou au début de toute exécution planifiée (consigne contenant « Mode routine »).
---

# Automatisation

## A. Tâches planifiées (une fois, dans Cowork)
1. Préparer une seule demande de validation V-… « Activation des tâches planifiées » listant les tâches ci-dessous.
2. Après « je valide » : si un outil de création de tâches planifiées est disponible dans la session, créer les tâches ;
   sinon, donner à Corentin la liste prête à copier-coller dans Cowork → Tâches planifiées.

| Nom | Quand | Consigne de la tâche | Modèle de la tâche |
|---|---|---|---|
| Point du jour | jours ouvrés 7 h 45 | `Charge le chef de cabinet. Mode routine : point du jour + tri des mails.` | le plus économe proposé (Haiku) |
| Prospection CRENOVIA | jours ouvrés 9 h 15 | `Charge le chef de cabinet. Mode routine : envoie la prospection CRENOVIA du jour.` | Haiku ou Sonnet |
| Suivi des réponses | jours ouvrés 17 h 30 | `Charge le chef de cabinet. Mode routine : lis les réponses aux e-mails, mets à jour le CRM, prépare les brouillons.` | Haiku |
| Point hebdo | lundi 8 h | `Charge le chef de cabinet. Mode routine : point hebdo.` | Sonnet |
| Clôture mensuelle | 1er du mois 8 h | `Charge le chef de cabinet. Mode routine : clôture mensuelle et échéances de chaque société.` | Sonnet |

- La prospection n'est proposée que si au moins un modèle M-CRENOVIA est ACTIF dans le registre d'`envois-automatiques`.
- Ces tâches tournent sur l'ordinateur de Corentin (Cowork ouvert), car le bureau est sur son OneDrive.

## B. Mode routine (à chaque exécution planifiée)
Quand la consigne contient « Mode routine » :
1. Ne pas faire le travail répétitif dans la conversation principale : le déléguer à l'agent compétent avec
   `model: haiku` et `effort: low` (lecture des mails, mise à jour des tableaux, préparation des envois, collecte des échéances).
2. Monter en `sonnet` seulement pour : rédaction d'un message personnalisé, synthèse hebdo ou mensuelle, anomalie à analyser.
   Jamais `opus` en routine : un sujet complexe (niveau 3) est mis de côté et signalé à Corentin pour une session dédiée.
3. Le Chef de cabinet se limite à : lancer, contrôler les retours compacts, écrire le rapport dans `_BUREAU_IA/rapports/`.
4. Ne sort que ce que permettent les modèles ACTIFS d'`envois-automatiques` ; tout le reste attend en brouillon dans la file de validation.
5. Rapport final de 15 lignes maximum. Si rien de neuf : une seule ligne.

## C. Choix du modèle hors routine
Automatique : le Chef de cabinet applique la grille « Économie » de CLAUDE.md à chaque délégation, sans rien demander.
Corentin peut forcer : « fais-le en économique » (Haiku) ou « fais-le à fond » (Opus).
