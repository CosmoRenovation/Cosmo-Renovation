---
name: envois-automatiques
description: Cadre des e-mails envoyés automatiquement sans validation au cas par cas (« solution 2 ») - registre des modèles pré-validés par Corentin, conditions de déclenchement, limites, journal d'envoi et arrêt d'urgence. À utiliser avant tout envoi automatique, pour faire valider un nouveau modèle, ou quand Corentin dit « stop envois ».
---

# Envois automatiques (modèles pré-validés)

Exception encadrée à la règle « rien ne sort sans validation » : Corentin valide **une fois** un modèle et ses
conditions ; ensuite les e-mails qui respectent **exactement** ce modèle et ces conditions partent sans nouvelle validation.

## Registre
`_BUREAU_IA/envois-automatiques/registre.md` — un bloc par modèle :

```
## M-<ENTITÉ>-<NN> — <nom>            Statut : ACTIF | SUSPENDU | BROUILLON
- Entité / adresse d'envoi :
- Déclencheur : (ex. ligne CRM « Statut envoi » = « À envoyer »)
- Destinataires autorisés : (ex. professionnels uniquement, adresse e-mail valide présente dans le CRM)
- Contenu : chemin du modèle · pièces jointes (chemins exacts)
- Personnalisation autorisée : (champs et phrases variables permis)
- Limites : max X envois / jour, plage horaire, jours ouvrés
- Validé par Corentin : V-… du AAAA-MM-JJ
```

Seuls les modèles **ACTIF** peuvent partir. Un modèle modifié (texte, pièces jointes, cible) repasse en BROUILLON et
doit être revalidé (nouvelle entrée V-…).

## Avant chaque envoi automatique (contrôles bloquants)
1. Le modèle est ACTIF et l'envoi respecte son déclencheur et ses destinataires autorisés.
2. Adresse e-mail présente et valide ; destinataire ni en opposition (`opposition.md`), ni déjà contacté par ce modèle.
3. Limite du jour non atteinte ; jour ouvré, entre 8 h 30 et 18 h.
4. Toutes les pièces jointes existent, sont la dernière version et pèsent < 20 Mo au total.
5. La personnalisation ne contient que des informations vérifiées (site de l'entité, CRM) — aucune invention.
Si un contrôle échoue : ne pas envoyer, laisser un brouillon et le signaler dans le point du jour.

## Après l'envoi
- Mettre à jour la ligne du CRM (statut, date, modèle) en suivant `bureau-de-gestion`.
- Ajouter une ligne à `_BUREAU_IA/envois-automatiques/journal-envois.md` :
  `date heure · modèle · destinataire · entité · objet · pièces jointes · id du message`.
- Réponse reçue → plus aucun envoi automatique à ce contact ; le signaler à Corentin (le suivi redevient manuel).
- Demande de désinscription / « ne plus me contacter » → ajouter à `opposition.md` immédiatement, statut CRM « Opposition ».
- Adresse en erreur (rebond) → statut CRM « Adresse invalide ».

## Arrêt d'urgence
« stop envois » (ou tout signal de problème : plainte, taux de rebond élevé, erreur dans un modèle) → passer tous les
modèles en SUSPENDU, ne plus rien envoyer, prévenir Corentin.

## Rapport
Le point du jour liste : envois de la veille par modèle, réponses, désinscriptions, erreurs.
