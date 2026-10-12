---
name: file-validation
description: Gère la file d'attente des validations de Corentin (bureau/validations/file.md) - créer une demande de validation avant toute action sortante (e-mail, envoi de document, signature, paiement, publication), afficher ce qui attend, et appliquer les réponses « je valide / je refuse / à revoir V-… ». Utiliser aussi quand Corentin tape /file-validation.
---

# File de validation

Principe : **Corentin valide, l'équipe exécute.** Aucune action sortante sans une ligne 🟢 VALIDÉ dans la file
ET une validation explicite dans la conversation en cours.

## Créer une demande
1. Préparer le livrable en **brouillon** (brouillon Gmail, fichier dans `bureau/rapports/` ou dossier de l'entité, page Notion brouillon).
2. Vérifier qu'il a été relu par `controleur-qualite` (obligatoire pour : e-mails à l'extérieur, documents juridiques,
   montants > 500 €, engagements de durée).
3. Attribuer l'ID `V-AAAAMMJJ-NN` (NN = compteur du jour, lire la file pour le prochain numéro).
4. Ajouter la ligne dans `bureau/validations/file.md` : entité, objet, type (e-mail / document / signature / paiement /
   décision / publication), préparé par, relu QC (oui/non + verdict), 🟡 EN ATTENTE, date, lien vers le brouillon.
5. Présenter à Corentin une **fiche de validation** courte :

```
🟡 V-20261012-01 — [Entité] Objet
Quoi : …               Pour qui : …
Pourquoi maintenant : …
Risques / points d'attention : … (verdict QC : OK / OK avec réserves)
Brouillon : <lien>
→ « je valide V-20261012-01 », « je refuse … », ou « à revoir … : ta remarque »
```

## Traiter une réponse
- **Valide** → statut 🟢, exécuter l'action (envoyer le brouillon, partager…), puis ✅ EXÉCUTÉ avec la date.
  Si c'est une décision, l'inscrire au journal (skill `journal-decisions`).
- **Refuse** → 🔴 + motif dans la colonne Lien/notes. Ne pas re-proposer la même chose sans élément nouveau.
- **À revoir** → 🔁, renvoyer à l'agent auteur avec la remarque mot pour mot, puis nouvelle fiche (même ID suffixé `-b`).
- Validation ambiguë (« ok », « vas-y » sans ID alors que plusieurs demandes attendent) → demander laquelle.

## Afficher la file
Lister les 🟡 par ordre d'ancienneté, puis les 🔁, avec l'âge en jours. Signaler tout ce qui attend depuis > 3 jours.
