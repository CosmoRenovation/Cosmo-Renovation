---
name: circuit-signature
description: Organise la signature d'un document - préparation de la version finale, contrôle, demande de validation à Corentin, envoi pour signature (électronique ou papier) et archivage. À utiliser chaque fois qu'un document doit être signé par Corentin ou un tiers.
---

# Circuit de signature

Inspiré de `signature-request` (anthropics/knowledge-work-plugins, Apache-2.0). Réécrit.

1. Version finale figée (PDF), nom de fichier `AAAA-MM-JJ_<entité>_<type>_<contrepartie>_v-finale.pdf`.
2. Contrôles : relecture contrat faite (`relecture-contrat`), bonnes parties / SIREN / adresses, montants cohérents,
   annexes jointes, bon signataire (qui a le pouvoir d'engager l'entité ?).
3. Fiche de validation V-… (type signature) avec résumé des engagements pris.
4. Après validation seulement : préparer l'envoi (outil de signature électronique si disponible, sinon e-mail en
   brouillon puis envoi après validation).
5. Suivi : relance à J+5 si non signé ; une fois signé → archiver dans le dossier de l'entité, noter dans la fiche,
   ajouter les échéances du contrat (fin, préavis) au calendrier des obligations.
