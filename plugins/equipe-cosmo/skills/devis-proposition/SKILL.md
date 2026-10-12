---
name: devis-proposition
description: Prépare un devis ou une proposition commerciale (rénovation, conception Créenovia, prestation Créaxia) clair, conforme aux mentions obligatoires, avec postes détaillés, prix, acomptes, délais et conditions, en brouillon pour validation. À utiliser dès qu'un client ou prospect demande un prix.
---

# Devis et proposition commerciale

Inspiré de `proposal-builder` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit pour le BTP / la conception en France.

1. **Brief** : client (particulier/pro), adresse du chantier, besoin, contraintes, budget annoncé, date souhaitée,
   visite faite ? photos / plans ?
2. **Chiffrage** : postes détaillés (fourniture / main-d'œuvre), quantités, prix unitaires, sous-traitance,
   marge visée (demander au `directeur-financier` le taux de marge cible) ; aléas.
3. **Mentions obligatoires** d'un devis de travaux et d'une facture — **vérifier la liste à jour** (service-public.fr,
   economie.gouv.fr) : identité, SIREN, assurance décennale (assureur, couverture géographique), TVA ou mention de
   franchise, taux de TVA réduit et attestation le cas échéant, durée de validité, modalités de paiement, droit de
   rétractation pour un contrat hors établissement avec un particulier.
4. **Proposition** : une page de présentation (compréhension du besoin, approche, planning, pourquoi nous), puis le devis.
5. Relecture `controleur-qualite` (calculs, mentions) → V-… → envoi après validation → suivi dans `suivi-prospects`.
