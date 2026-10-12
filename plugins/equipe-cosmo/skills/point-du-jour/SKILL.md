---
name: point-du-jour
description: Point quotidien court pour Corentin - ce qui a avancé depuis hier, ce qui attend sa validation, ce qui bloque, les échéances des 7 prochains jours, toutes entités confondues. À utiliser quand Corentin tape /point-du-jour, demande « on en est où ? », ou lors d'une exécution planifiée le matin.
---

# Point du jour

Inspiré de `monday-brief` / `business-pulse` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

## Sources à lire
1. `bureau/validations/file.md` (🟡 et 🔁)
2. `bureau/taches.md` (échéances ≤ 7 jours, retards)
3. Échéances des fiches `bureau/entites/*.md`
4. Les rapports d'hier dans `bureau/rapports/`
5. Si connecteurs disponibles : agenda du jour, e-mails non lus importants (lecture seule).

## Format (tient sur un écran de téléphone)

```
☀️ Point du AAAA-MM-JJ

À VALIDER (n)
• V-… [Entité] objet — depuis X j
AVANCÉ
• [Entité] …
BLOQUÉ / BESOIN DE TOI
• … → ce qu'il faut : …
ÉCHÉANCES 7 JOURS
• JJ/MM [Entité] …
PROPOSITION DU JOUR
• 1 action à plus forte valeur
```

Enregistrer dans `bureau/rapports/AAAA-MM-JJ-point-du-jour.md`. Si rien de neuf : le dire en une ligne.
