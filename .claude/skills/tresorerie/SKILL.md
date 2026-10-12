---
name: tresorerie
description: Photo et prévision de trésorerie à 30/60/90 jours par entité - encaissements attendus, décaissements (fournisseurs, URSSAF, TVA, impôts, loyers, prêts), point bas et alertes. À utiliser quand Corentin parle d'argent disponible, avant une dépense importante, avant un achat de matériaux, ou chaque semaine.
---

# Trésorerie

Inspiré de `cash-flow-snapshot` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

1. **Solde de départ** : demander le solde bancaire du jour (ou relevé fourni). Ne jamais l'inventer.
2. **Encaissements** : factures émises non payées (date d'échéance réaliste, pas théorique), acomptes de devis signés.
3. **Décaissements** : fournisseurs et matériaux, sous-traitants, charges fixes (loyer, assurances, abonnements,
   véhicule, prêt), cotisations URSSAF, TVA, impôts — dates issues du calendrier `suivi-obligations`.
4. **Tableau semaine par semaine** sur 13 semaines (xlsx si demandé) + solde projeté.
5. **Alertes** : semaine où le solde passe sous le seuil de sécurité (à définir avec Corentin, par défaut 1 mois de
   charges fixes) → actions proposées : relancer (`relance-factures`), décaler un achat, demander un acompte.
6. Mettre à jour « Chiffres clés » de la fiche entité.
