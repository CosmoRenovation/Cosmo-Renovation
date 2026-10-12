---
name: relance-factures
description: Repère les factures clients impayées ou en retard et prépare des relances graduées (rappel courtois, relance ferme, mise en demeure) en brouillon pour validation. À utiliser chaque semaine, quand la trésorerie est tendue, ou quand Corentin mentionne un client qui ne paie pas.
---

# Relance des factures

Inspiré de `invoice-chase` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

1. Lister les factures : client, n°, montant TTC, échéance, jours de retard, relances déjà faites.
2. Niveau de relance :
   - J+1 à J+15 : rappel courtois (oubli possible), facture jointe ;
   - J+15 à J+30 : relance ferme, rappel des pénalités prévues aux conditions de paiement ;
   - > J+30 ou 2 relances sans effet : mise en demeure (préparée avec le `juriste`).
   Adapter : particulier ≠ professionnel (pénalités et indemnité forfaitaire de 40 € concernent les pros — vérifier).
3. Rédiger chaque relance en **brouillon** (Gmail si connecté), ton adapté à la relation client.
4. Une entrée V-… par lot de relances (type e-mail). Rien n'est envoyé avant validation.
5. Après envoi validé : noter la date de relance ; prévoir la suivante.
