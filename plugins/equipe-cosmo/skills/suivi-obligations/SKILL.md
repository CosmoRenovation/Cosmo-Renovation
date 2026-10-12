---
name: suivi-obligations
description: Tient le calendrier des obligations légales, sociales et fiscales de chaque entité (déclarations URSSAF, TVA, liasse, approbation des comptes, dépôt au greffe, assurances, AG, CFE…) et alerte avant échéance. À utiliser lors de la création d'une entité, chaque mois, et dans les points du jour/hebdo.
---

# Suivi des obligations

Inspiré de `compliance-tracking` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

1. Pour chaque entité, établir la liste des obligations selon sa forme et son régime (micro, SAS à l'IS, SCI à l'IR
   ou à l'IS, holding) — **vérifier sur urssaf.fr, impots.gouv.fr, service-public.fr** et noter l'URL et la date.
2. Les inscrire dans le tableau « Échéances » de la fiche `bureau/entites/<entité>.md`
   (date · obligation · responsable · statut).
3. Alerte J-15 et J-3 dans le point du jour. Échéance dépassée → 🔴 en tête du point.
4. Une fois par trimestre : revérifier la liste (changements de seuils, de régime, nouvelle activité).

Ce skill organise ; la déclaration elle-même est préparée par le `directeur-financier` et validée par Corentin.
