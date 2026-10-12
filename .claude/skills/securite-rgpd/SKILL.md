---
name: securite-rgpd
description: Vérifie la sécurité informatique et la conformité RGPD des entités (mots de passe, double authentification, sauvegardes, accès des agents IA, données clients, mentions légales et politique de confidentialité du site, registre des traitements). À utiliser à la mise en place d'un outil, d'un site, ou lors d'un audit trimestriel.
---

# Sécurité et RGPD

Inspiré de `ciso-advisor` (alirezarezvani/claude-skills, MIT). Réécrit, adapté TPE.

## Check-list sécurité (TPE)
- Gestionnaire de mots de passe ; double authentification sur e-mail, banque, Google, outils de facturation.
- Sauvegardes (règle 3-2-1) des documents des entités ; test de restauration.
- Accès des agents IA : connecteurs limités au nécessaire, **aucun skill/plugin tiers non relu**, revue des
  autorisations chaque trimestre.
- Appareils à jour, chiffrement du disque, verrouillage.

## RGPD
- Registre des traitements simplifié (clients, prospects, fournisseurs, salariés) : données, finalité, durée, outils.
- Site web : mentions légales, politique de confidentialité, bandeau cookies si traceurs (référence : cnil.fr).
- Devis/factures : ne collecter que le nécessaire ; durées de conservation (à vérifier : obligations comptables).

Livrable : tableau ✅/⚠️/❌ avec actions priorisées, rien n'est modifié sans validation.
