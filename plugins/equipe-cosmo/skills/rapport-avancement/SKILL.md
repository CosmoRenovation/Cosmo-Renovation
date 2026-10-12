---
name: rapport-avancement
description: Rédige un compte rendu d'avancement d'un projet précis (une entité ou un chantier) - objectif, fait, à faire, risques, besoins de décision. À utiliser quand Corentin demande où en est un projet, ou pour informer un tiers (associé, comptable, banquier) après validation.
---

# Rapport d'avancement

Inspiré de `status-report` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

Structure :
1. **Objectif** du projet et date cible.
2. **Météo** : 🟢 / 🟡 / 🔴 avec une phrase de justification.
3. **Fait depuis le dernier point** (faits vérifiables, liens).
4. **À faire** (prochaines étapes, responsable, date).
5. **Risques** et parade.
6. **Décisions attendues de Corentin** → chacune en entrée de la file de validation.

Destinataire interne : 1 page max. Destinataire externe : passe par `controleur-qualite` puis `file-validation`.
