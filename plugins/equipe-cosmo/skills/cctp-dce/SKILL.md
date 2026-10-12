---
name: cctp-dce
description: Rédige les pièces de consultation des entreprises pour une mission AMO CRENOVIA - CCTP par lot, DPGF (cadre de décomposition des prix), règlement de consultation et lettre de consultation - à partir du programme de travaux validé. À utiliser quand un programme de travaux est arrêté et qu'il faut consulter des entreprises.
---

# CCTP et DCE (CRENOVIA)

## Prérequis
Programme de travaux validé par le client (compte rendu de visite, scénario retenu, budget). Sinon, le demander d'abord.
Rappel métier : l'AMO ne conçoit pas les ouvrages. Si le projet nécessite une conception (structure, permis), signaler
qu'il faut un maître d'œuvre / architecte / bureau d'études.

## Pièces produites (dossier `DCE_<Projet>/`)
1. **CCTP par lot** (Word) : généralités (objet, documents de référence, normes et DTU applicables — citer ceux
   réellement concernés, à vérifier), description des ouvrages par poste, matériaux et performances attendues
   (ex. résistance thermique visée pour l'éligibilité aux aides — valeurs à vérifier sur les sources officielles),
   mise en œuvre, interfaces avec les autres lots, essais et réception.
   Lots types : démolition/curage · gros œuvre · charpente/couverture · menuiseries ext. · isolation/plâtrerie ·
   électricité · plomberie/CVC · revêtements · peinture.
2. **DPGF par lot** (Excel) : mêmes postes que le CCTP, colonnes Unité · Quantité · PU HT · Total HT, totaux par lot,
   TVA (taux à confirmer selon la nature des travaux), total TTC. Quantités issues du relevé ; sinon « à métrer ».
3. **Règlement de consultation** : objet, lots, date limite, pièces à fournir (attestations d'assurance décennale et
   RC pro, Kbis, références, RGE si aides visées), critères de jugement (prix, valeur technique, délai), visite de site.
4. **Lettre de consultation** (e-mail en brouillon par entreprise).

## Qualité
- Même numérotation de postes entre CCTP et DPGF (contrôle croisé).
- `controleur-qualite` niveau 2 (niveau 3 si budget > 50 k€).
- Envoi aux entreprises seulement après validation du client et de Corentin (V-…).
