---
name: prospection-crenovia
description: Campagne d'e-mails de présentation de CRENOVIA (AMO et conseil en rénovation, Caen) envoyés automatiquement aux contacts du tableau CRM du dossier Commerciale de CRENOVIA, avec mail d'introduction adapté (contact générique ou personne nommée), fiche de prestation globale, présentation CRENOVIA et fiche de prestation propre au type de client en pièces jointes. À utiliser pour préparer, faire valider, lancer, suivre ou arrêter la prospection CRENOVIA.
---

# Prospection CRENOVIA

S'appuie sur `envois-automatiques` (règles, limites, journal) et `bureau-de-gestion` (fichiers, copies, traçabilité).

## Ce qu'on sait de CRENOVIA (source : présentation CRENOVIA, Drive, août 2026)
- **CRENOVIA** — Conseil, Coordination et Réalisation en Rénovation Énergétique. Assistance à maîtrise d'ouvrage (AMO)
  et conseil en rénovation, **Caen · Calvados · Normandie**. Entreprise individuelle, SIRET 933 598 393 00017, APE 7490A, RC Pro.
- Corentin REBY, ingénieur bâtiment (Builders École d'Ingénieurs) ; terrain gros œuvre et rénovation (Eiffage, Cuénod
  Constructions Genève, Cosmo Rénovation), diagnostics et réhabilitation de logements.
- Prestations : études préalables & diagnostic ; programme & budget ; montage de dossiers d'aides (MaPrimeRénov', CEE,
  aides locales) et DCE ; assistance technique & administrative jusqu'à la réception. Mission complète ou séquencée.
- Arguments : indépendance (aucune commission sur les travaux), interlocuteur unique, ancrage local, premier échange
  gratuit, proposition écrite sous 7 jours.
- Références : gîte à Ver-sur-Mer (3 bâtiments), corps de ferme à Clécy, logements sociaux en Normandie.
- Contact : 06 33 74 33 71 · www.crenovia.com · 11 rue Saint-Sauveur, 14000 Caen.
  ⚠️ La présentation indique deux adresses e-mail (crenovia.fr@gmail.com et crenovia@gmail.com) : faire confirmer
  la bonne par Corentin et corriger la présentation.

## 1. Préparation (une fois)
1. **Localiser** dans le bureau le dossier `CRENOVIA/Commerciale/` (ou équivalent) et noter son chemin dans `carte-du-bureau.md`.
2. **Le CRM** : ouvrir le tableau en lecture, repérer les colonnes (entité, nom du contact, fonction, e-mail, type de client,
   ville, site web, statut d'envoi, dates, notes). S'il manque des colonnes nécessaires, **proposer** (validation) d'ajouter :
   `Type de client` · `Contact nommé (oui/non)` · `Statut envoi` · `Date envoi` · `Modèle` · `Réponse` · `Opposition`.
   Valeurs de `Statut envoi` : À qualifier · **À envoyer** · Envoyé · Réponse · Opposition · Adresse invalide · Manuel.
3. **Les pièces jointes** (PDF, dernières versions) — chemins à inscrire dans le registre :
   - `Presentation_CRENOVIA.pdf` (export PDF de la présentation Google Slides « CRENOVIA_Presentation ») ;
   - `Fiche_Prestation_Globale_CRENOVIA.pdf` ;
   - une `Fiche_Prestation_<Type>.pdf` par type de client.
   Lister à Corentin les fiches manquantes ; l'équipe peut les rédiger (skill docx/pdf) à partir de la présentation, puis validation.
4. **Correspondance type de client → fiche**, à confirmer avec Corentin (types proposés) :

| Type de client | Angle du message | Fiche |
|---|---|---|
| Architecte / maître d'œuvre | partenariat : diagnostics, programmes, chiffrage, dossiers d'aides en appui ; mission réduite PC/DP | Fiche_Prestation_Architectes |
| Bailleur social / collectivité | diagnostics et programmes de travaux de réhabilitation, montage des aides | Fiche_Prestation_Bailleurs_Collectivites |
| Syndic / copropriété | audit, plan pluriannuel de travaux, aides collectives, consultation des entreprises | Fiche_Prestation_Coproprietes |
| Agence immobilière / investisseur / SCI | chiffrage avant achat, programme de rénovation, valorisation | Fiche_Prestation_Investisseurs |
| Hébergement touristique (gîtes, hôtels) | rénovation par bâtiment, phasage hors saison (référence Ver-sur-Mer) | Fiche_Prestation_Hebergement |
| Entreprise du BTP | co-traitance, AMO pour leurs clients, apport d'affaires | Fiche_Prestation_Entreprises |

## 2. Le mail d'introduction
**Deux variantes**, choisies automatiquement :
- **Précise** — le CRM donne une personne nommée (nom + fonction) : « Bonjour Madame/Monsieur <Nom>, », référence à son
  rôle et, si vérifiable sur le site de l'entité, à un projet ou une spécialité réelle (une phrase, sourcée).
- **Large** — adresse générique (contact@, accueil@) : « Bonjour, » + demande de transmission à la personne en charge
  des projets de rénovation / travaux.

Trame (≤ 150 mots, vouvoiement, ton direct) :

```
Objet : <Accroche selon le type> — CRENOVIA, AMO rénovation à Caen

Bonjour <Madame/Monsieur Nom | ,>

<Phrase personnalisée : qui vous êtes / ce que fait l'entité (vérifié)>.

Je suis Corentin REBY, ingénieur bâtiment et fondateur de CRENOVIA, structure indépendante d'assistance à maîtrise
d'ouvrage basée à Caen. <1-2 phrases sur ce que CRENOVIA apporte à CE type de client>.

<1 référence pertinente : Ver-sur-Mer / Clécy / logements sociaux>.

Vous trouverez en pièces jointes ma présentation, notre fiche de prestations et une fiche dédiée à <type de client>.
Seriez-vous disponible pour un premier échange de 20 minutes, sans engagement, dans les prochaines semaines ?

[Version large : Si vous n'êtes pas la bonne personne, pourriez-vous transmettre ce message au responsable des projets
de travaux ? Merci par avance.]

Bien cordialement,
Corentin REBY — CRENOVIA · Assistance à maîtrise d'ouvrage
06 33 74 33 71 · www.crenovia.com · 11 rue Saint-Sauveur, 14000 Caen

Vous recevez ce message en raison de votre activité professionnelle. Pour ne plus recevoir de messages de CRENOVIA,
répondez simplement « STOP ».
```

## 3. Validation (une fois par type de client)
Pour chaque type : générer **2 exemples réels** (un précis, un large) avec les vraies pièces jointes, en brouillons
Gmail ; `controleur-qualite` relit ; entrée V-… « Activation modèle M-CRENOVIA-<NN> » avec : texte, pièces jointes,
cible, limite/jour. Après « je valide », inscrire le modèle ACTIF dans le registre d'`envois-automatiques`.

## 4. Envoi automatique (tâche planifiée Cowork, jours ouvrés)
Pour chaque ligne du CRM au statut **À envoyer**, dans l'ordre de priorité, jusqu'à la limite du jour
(**10/jour les 2 premières semaines**, puis 20/jour si aucun problème — protège la réputation de l'adresse d'envoi) :
1. Contrôles bloquants d'`envois-automatiques` + type de client connu + fiche correspondante présente.
2. **Professionnels uniquement.** Un particulier ne reçoit jamais d'e-mail de prospection automatique
   (consentement préalable requis — vérifier sur cnil.fr) → statut « Manuel ».
3. Contact sans e-mail (formulaire de site uniquement) → statut « Manuel » et ajout à la liste « à faire à la main » du point du jour.
4. Rédiger selon la variante, joindre les 3 PDF, envoyer depuis l'adresse CRENOVIA validée.
5. Mettre à jour le CRM (Envoyé, date, modèle) + journal d'envois.

## 5. Suivi
- Chaque matin : lire les réponses (Gmail), passer le contact en « Réponse », résumer à Corentin, préparer une réponse en
  **brouillon** (jamais automatique).
- Relance unique à J+10 sans réponse : uniquement si un modèle de relance a été validé séparément (M-CRENOVIA-R1).
- Bilan hebdo : envoyés, taux de réponse par type de client, rendez-vous obtenus → ajuster les messages (nouvelle validation).
