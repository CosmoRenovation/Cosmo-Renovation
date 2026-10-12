---
name: cloture-mensuelle
description: Prépare la fin de mois de chaque entité - pièces manquantes, rapprochement bancaire, factures émises/reçues, chiffre d'affaires à déclarer (micro), TVA, envoi au comptable, tableau de bord du mois. À utiliser en fin ou début de mois.
---

# Clôture mensuelle

Inspiré de `close-month` / `month-end-prep` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

Check-list par entité :
1. Toutes les factures émises du mois numérotées sans trou ; devis signés → factures d'acompte faites.
2. Factures fournisseurs / tickets récupérés pour chaque dépense bancaire (lister les manquants à Corentin).
3. Rapprochement : chaque ligne bancaire ↔ une pièce.
4. Micro-entreprise : CA encaissé du mois/trimestre pour la déclaration URSSAF (vérifier périodicité choisie).
   Suivi du cumul annuel vs seuils micro et seuils de franchise de TVA (valeurs à vérifier sur les sites officiels).
5. Sociétés : pièces à transmettre à l'expert-comptable, TVA du mois si régime réel mensuel.
6. Tableau de bord : CA, marge brute chantier, charges, résultat estimé, trésorerie, comparaison au mois précédent.
7. Rapport dans `bureau/rapports/AAAA-MM-cloture-<entité>.md` ; échéances reportées dans `suivi-obligations`.
