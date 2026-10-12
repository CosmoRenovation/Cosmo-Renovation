---
name: chiffrage-amo
description: Estime le coût des travaux d'un projet de rénovation par scénario (minimal / intermédiaire / performant) à partir de la base de prix CRENOVIA_Base_Prix_BTP et des quantités relevées, avec aides mobilisables et reste à charge, pour le programme et le budget d'une mission AMO. À utiliser après une visite, pour bâtir un programme de travaux ou répondre à « combien ça va coûter ? ».
---

# Chiffrage AMO (CRENOVIA)

## Sources
- **Base de prix** : `CRENOVIA_Base_Prix_BTP` (Google Sheets sur le Drive de Corentin ; ou copie dans le bureau).
  Lire sa structure à la première utilisation et la décrire dans `carte-du-bureau.md`.
- **Quantités** : compte rendu de visite, plans, relevés. Une quantité estimée est marquée « estimée » avec l'hypothèse.
- Prix absent de la base → fourchette issue de sources publiques identifiées, marquée « hors base — à confirmer »,
  et proposition d'ajouter le prix à la base (validation).

## Méthode
1. Lister les postes par lot (même découpage que `cctp-dce`).
2. Construire **3 scénarios** : minimal (mise en sécurité / urgences), intermédiaire, performant (rénovation globale).
3. Pour chaque poste : quantité × prix unitaire de la base, + aléas (10 % par défaut, 15-20 % en bâti ancien), + honoraires
   (maîtrise d'œuvre, bureaux d'études, diagnostics, AMO) en lignes séparées.
4. **Aides** : identifier les aides potentiellement mobilisables (MaPrimeRénov', CEE, aides locales) — conditions et
   montants **vérifiés sur les sites officiels à la date du jour**, sinon « à vérifier » ; jamais de montant de mémoire.
5. **Restitution** : tableau Excel par scénario (HT, TVA à confirmer, TTC, aides estimées, reste à charge) + une page de
   synthèse pour le client, avec les hypothèses et la marge d'incertitude (± 15 à 25 % à ce stade).
6. `controleur-qualite` refait les totaux ; envoi au client après validation (V-…).
