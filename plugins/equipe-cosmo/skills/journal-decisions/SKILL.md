---
name: journal-decisions
description: Inscrit les décisions validées par Corentin dans bureau/decisions/journal.md et permet de les retrouver (par entité, sujet, échéance). À utiliser après chaque validation d'une décision, quand Corentin demande « qu'est-ce qu'on avait décidé sur … », ou pour vérifier les actions en retard.
---

# Journal des décisions

Inspiré de `decision-logger` (alirezarezvani/claude-skills, MIT). Réécrit, sans script.

## Règles
- On n'inscrit **que** ce que Corentin a validé. Les débats, options écartées et brouillons restent dans `bureau/rapports/`.
- Append-only : une décision n'est jamais effacée ; si elle change, l'ancienne passe en « remplacée par D-… ».
- Avant de proposer quelque chose, les agents vérifient qu'il n'existe pas déjà une décision active contraire.
  S'il y en a une : le signaler explicitement au lieu de la contourner.

## Inscrire
Ajouter en fin de `bureau/decisions/journal.md` selon le modèle du fichier (ID `D-AAAAMMJJ-NN`, entité, décision en
une phrase, pourquoi, responsable, échéance, date de revue, validation V-… liée, statut). Ajouter la tâche
correspondante dans `bureau/taches.md`.

## Rechercher
Filtrer par entité / mot-clé ; répondre avec l'ID, la date et la décision. Lister les décisions dont l'échéance ou la
date de revue est passée → à remonter dans le prochain point.
