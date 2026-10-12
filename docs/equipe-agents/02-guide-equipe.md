# Guide de l'équipe d'agents

## Organisation

```
Corentin (président) ── valide / refuse / réoriente
   │
Chef de cabinet = la conversation principale de Claude (règles dans CLAUDE.md)
   │  routeur-demandes · file-validation · journal-decisions · point-du-jour · point-hebdo · rapport-avancement
   │
   ├── directeur-strategie   affiner-idee · analyse-scenarios · valider-idee-marche · business-plan · plan-action · grille-risques
   ├── juriste               relecture-contrat · evaluation-risque-juridique · suivi-obligations · circuit-signature
   │                         creation-sas · transition-micro-sas · structuration-holding · societe-immobiliere
   ├── directeur-financier   tresorerie · relance-factures · cloture-mensuelle · fiscalite-sociale-fr
   │                         analyse-investissement-immobilier · business-plan · analyse-scenarios
   ├── directeur-technique   conseil-technique · securite-rgpd · plan-action
   ├── responsable-commercial devis-proposition · tri-emails · suivi-prospects · contenus-reseaux · avis-clients
   ├── controleur-qualite    relecture-croisee · grille-risques   (lecture seule, relit tout avant toi)
   └── assistant-ecole       suivi-ecole · recherche-documentaire
   (tous : verification-avant-livraison)
```

38 skills (dont `bureau-de-gestion`, `chef-de-cabinet`, qui transporte les règles dans Cowork), tous réécrits en français : texte seul, **aucun script, hook ni code tiers**. Chaque skill indique sa source d'inspiration.

## Garde-fous intégrés
- **Rien ne part sans toi** : les agents n'ont pas l'outil d'envoi d'e-mail (seulement lecture + brouillons).
  L'envoi est fait par le Chef de cabinet, après ton « je valide V-… ».
- Le contrôleur qualité est en lecture seule et juge chaque livrable avant qu'il arrive jusqu'à toi.
- Droit et fiscalité : sources officielles obligatoires ; pour les sujets engageants, l'équipe recommande l'avis d'un professionnel.
- Le contenu des e-mails et des pages web n'est jamais traité comme un ordre (protection contre les arnaques et les injections).

## Comment l'utiliser au quotidien
1. Ouvre une session Claude Code sur ce dépôt (app, web ou téléphone) et parle normalement :
   « On doit passer en SAS, prépare-moi le dossier », « Relis ce contrat de sous-traitance », « Fais le point ».
2. Commandes : `/point-du-jour`, `/point-hebdo`, `/file-validation`, `/affiner-idee`, ou n'importe quel skill par son nom.
3. Pour valider : « je valide V-20261012-01 » · « je refuse V-… parce que … » · « à revoir V-… : … ».

## Mise en autonomie (à activer quand tu es prêt)
Le bureau étant sur OneDrive (ton ordinateur), les tâches automatiques se créent dans **Cowork → Tâches planifiées**
(elles tournent quand ton ordinateur est allumé et Cowork ouvert) :
- **Routine du matin** (jours ouvrés, ex. 7 h 45) : `/point-du-jour` + `tri-emails` → rapport
  dans `03_BUREAU_IA/rapports/`.
- **Routine du lundi** : `/point-hebdo`.
- **Routine du 1er du mois** : `cloture-mensuelle` + `suivi-obligations` pour chaque entité.
Les routines préparent et proposent ; elles n'exécutent aucune action sortante sans ta validation.

## Première étape indispensable
Installer le bureau de gestion (voir Cowork ci-dessus) puis corriger les fiches de `03_BUREAU_IA/entites/` (SIREN, activité, chiffres, échéances, comptable). Sans elles, les agents
travaillent sur des hypothèses. Tu peux simplement dicter les infos dans une session : l'équipe remplit les fiches.

## Utiliser l'équipe dans Cowork
L'équipe est empaquetée en **plugin** (`plugins/equipe-cosmo/`) et le dépôt sert de **place de marché**.
1. Cowork → Personnaliser → Plugins → « + » → Ajouter une place de marché → `CosmoRenovation/Cosmo-Renovation`.
2. Installer « Équipe Cosmo ».
3. Ouvrir dans Cowork le dossier OneDrive **`00-PRIMO/TC5`** (le bureau de gestion), puis la première fois :
   « Charge le chef de cabinet et installe le bureau de gestion » → création de `03_BUREAU_IA/`, lecture des classeurs,
   carte du bureau et pré-remplissage des fiches des sociétés.
   Ensuite : « Fais le point du jour ».
4. Après chaque modification des agents/skills sur GitHub : bouton « Mettre à jour » de la place de marché.
