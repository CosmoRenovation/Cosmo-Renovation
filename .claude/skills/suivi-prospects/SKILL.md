---
name: suivi-prospects
description: Tient le suivi des prospects et devis (pipeline - contact, visite, devis envoyé, relance, signé, perdu), priorise les relances et calcule le CA potentiel. À utiliser chaque semaine et après chaque nouveau contact ou devis.
---

# Suivi des prospects

Inspiré de `crm-autopilot` / `lead-triage` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

- Tableau par entité dans `bureau/` (ou Notion/Asana si Corentin le choisit) : prospect, source, besoin, montant,
  étape, prochaine action + date, probabilité.
- Chaque semaine : devis envoyés sans réponse depuis 7 jours → relance en brouillon ; prospects chauds en tête ;
  CA pondéré du mois.
- Devis perdu : noter la raison (prix, délai, concurrent) pour l'analyse trimestrielle.
