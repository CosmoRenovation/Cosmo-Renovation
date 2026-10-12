---
name: relecture-contrat
description: Relit un contrat ou document engageant (devis signé, contrat de sous-traitance, bail, CGV, contrat de prestation, statuts, pacte, offre de prêt) et produit une analyse clause par clause avec niveau de risque et propositions de modification. À utiliser dès qu'un document va être signé ou envoyé pour signature.
---

# Relecture de contrat

Inspiré de `review-contract` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit pour le droit français.

## Étapes
1. **Identifier** : type de contrat, parties, entité du groupe concernée, qui l'a rédigé, enjeu financier, durée.
2. **Lire en entier.** Pas d'analyse sur un extrait.
3. **Points à contrôler systématiquement** :
   - objet et périmètre précis ; prix, révision, modalités et délais de paiement (pénalités de retard, indemnité
     forfaitaire de recouvrement pour les pros) ;
   - durée, reconduction tacite, résiliation et préavis ;
   - responsabilité et plafonds, assurances (pour le BTP : décennale, RC pro, garantie de parfait achèvement) ;
   - pénalités, garanties, retenue de garantie ; sous-traitance (loi de 1975 si BTP) ;
   - propriété intellectuelle (Crenovia : plans et conceptions !) ; confidentialité ; non-concurrence ;
   - droit applicable, juridiction, médiation ; mentions obligatoires selon le type (devis, bail…).
4. **Tableau** : clause · ce qu'elle dit (en clair) · risque 🟢/🟡/🔴 · proposition de modification.
5. **Synthèse** : signer en l'état / signer avec modifications / ne pas signer, et les 3 points à négocier en priorité.
6. Contrat à fort enjeu (> 10 k€, durée > 1 an, statuts, pacte, bail commercial, prêt) → recommander une relecture par
   un avocat et le dire clairement.

Ne jamais signer ou faire signer : passer par `circuit-signature`.
