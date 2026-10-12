---
name: compte-rendu-visite
description: Transforme les notes de visite de Corentin (dictées, tapées ou en vrac) et ses photos en compte rendu de visite technique / diagnostic CRENOVIA propre, au format Word ou PDF - état des lieux par ouvrage, désordres, contraintes réglementaires, premières préconisations, photos légendées. À utiliser après chaque visite de site, état des lieux ou diagnostic.
---

# Compte rendu de visite (CRENOVIA)

## Entrées
- Notes de Corentin (même désordonnées, dictées depuis le téléphone), photos, adresse, date, client, type de bien.
- Fiche du projet dans le bureau (`CRENOVIA_Suivi_Operationnel.xlsx`) si elle existe.
Ne rien inventer : ce qui n'est pas dans les notes ou les photos est marqué « non relevé » ou « à vérifier ».

## Structure du document
1. **En-tête** : CRENOVIA (logo si disponible), titre, référence `CRV-AAAAMMJJ-<client>`, date de visite, présents,
   adresse, maître d'ouvrage, type de bien, année de construction (si connue), surface.
2. **Objet de la visite** (2-3 lignes).
3. **Synthèse** (encadré, 5 lignes max) : état général, 3 points majeurs, urgences éventuelles.
4. **État des lieux par ouvrage** — tableau : Ouvrage · Constat · État (Bon / Moyen / Dégradé / Hors service) · Photo n° ·
   Préconisation. Ouvrages : structure/gros œuvre, toiture/couverture, façades, menuiseries extérieures, isolation,
   chauffage/ECS, ventilation, électricité, plomberie, second œuvre, extérieurs.
5. **Contraintes réglementaires repérées** : amiante/plomb (selon année de construction), urbanisme (PLU, ABF), accessibilité,
   incendie, performance énergétique — en signalant les diagnostics obligatoires à faire réaliser.
6. **Premières préconisations et suite proposée** (scénarios de travaux à étudier, investigations complémentaires).
7. **Annexe photos** : photos numérotées et légendées.
8. Pied de page : CRENOVIA · SIRET · contact · « Document établi sur la base d'un examen visuel non destructif ».

## Production
- Format : PDF (skill pdf) pour envoi, ou Word (skill docx) si Corentin veut retoucher. Fichier :
  `CRV_AAAA-MM-JJ_<Client>.pdf` dans le dossier du projet.
- Relecture `controleur-qualite` (niveau 2) ; envoi au client uniquement après validation (V-…).
- Mettre à jour le suivi opérationnel : « Visite faite le … — CR rédigé ».
