---
name: evaluation-risque-juridique
description: Évalue un risque juridique (litige client, impayé, malfaçon, conformité, responsabilité du dirigeant, choix de structure) - probabilité, gravité, options et coût de chaque option. À utiliser face à un problème juridique ou avant une décision qui engage juridiquement.
---

# Évaluation de risque juridique

Inspiré de `legal-risk-assessment` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

1. **Faits** : chronologie, pièces disponibles, montants, entité concernée. Séparer faits prouvés et affirmations.
2. **Règles applicables** : rechercher sur Légifrance / service-public.fr, citer article et URL.
3. **Risque** : probabilité (faible/moyenne/forte) × gravité (€, réputation, responsabilité personnelle de Corentin).
4. **Options** : ne rien faire / négocier / mise en demeure / médiation / action en justice — coût, délai, chances.
5. **Recommandation** et prochaines actions datées ; préparer en brouillon les courriers éventuels
   (mise en demeure → `controleur-qualite` puis `file-validation`).
6. Indiquer quand un avocat est nécessaire (au-delà de la compétence générale, procédure engagée, enjeu élevé).
