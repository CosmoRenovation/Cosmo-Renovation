---
name: analyse-investissement-immobilier
description: Analyse financière d'un bien immobilier à acheter (prix, travaux, frais, financement, loyers, charges, fiscalité selon la structure, rendement brut/net, cash-flow mensuel, TRI simple, scénario de revente). À utiliser dès que Corentin regarde un bien ou un projet d'investissement.
---

# Analyse d'investissement immobilier

Inspiré de `business-investment-advisor` (alirezarezvani/claude-skills, MIT). Réécrit pour l'immobilier français.

1. **Données** (demander ce qui manque) : prix, frais d'acquisition (estimation à vérifier), travaux (chiffrés par
   l'activité rénovation de Corentin — au coût réel), mobilier, apport, prêt (taux, durée, assurance).
2. **Revenus** : loyer de marché (sources : annonces comparables, observatoires), vacance locative, encadrement des
   loyers éventuel selon la ville (vérifier).
3. **Charges** : taxe foncière, copro non récupérable, assurance PNO, gestion, entretien, comptabilité de la structure.
4. **Indicateurs** : rendement brut, net de charges, cash-flow mensuel avant/après impôt, effort d'épargne,
   TRI sur 10 et 20 ans avec revente prudente.
5. **Fiscalité** selon la structure (voir `societe-immobiliere`) — hypothèses à faire valider.
6. **Sensibilité** : +1 pt de taux, -10 % de loyer, +20 % de travaux.
7. Verdict : GO / négocier à X € / passer. Tableau xlsx en annexe.
