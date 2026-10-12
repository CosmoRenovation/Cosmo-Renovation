# Catalogue des skills GitHub — présélection pour l'équipe d'agents

> Étape 1 sur 3 : **repérer** → 2 : **sélectionner ensemble** → 3 : **réécrire nous-mêmes** (aucun code tiers exécuté).
> Recherche faite le 12/10/2026. Les dépôts ont été lus en lecture seule ; aucun script n'a été exécuté.

## 1. Dépôts sources retenus

| Code | Dépôt | Contenu | Fiabilité | Risque technique |
|---|---|---|---|---|
| **A** | [anthropics/skills](https://github.com/anthropics/skills) | 19 skills officiels (docx, xlsx, pptx, pdf, rédaction, création de skills) | Officiel Anthropic | Faible — scripts Python de conversion de fichiers |
| **K** | [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins) | ~250 skills métier : juridique, finance, ops, RH, marketing, ventes, **petite entreprise** | Officiel Anthropic | Faible — quasi uniquement du texte (SKILL.md) |
| **R** | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) | ~1 000 skills/agents : direction (CEO, CFO, COO, juriste…), gestion de projet, conformité | Communautaire (très populaire) | **Élevé** — 774 scripts, 14 fichiers de hooks/settings, appels réseau |
| **V** | [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) | Agents « personnages » : chef de projet, analyste, orchestrateurs | Communautaire | Faible — fichiers Markdown seulement |
| **W** | [wshobson/agents](https://github.com/wshobson/agents) | Plugins dont `agent-teams` (chef d'équipe / exécutant / relecteur) | Communautaire | Moyen — quelques hooks et scripts |
| **S** | [obra/superpowers](https://github.com/obra/superpowers) | Méthode : brainstorming, plans, vérification avant de dire « fini » | Communautaire (référence) | Moyen — 1 hook de démarrage, scripts |
| **M** | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 50 skills marketing / acquisition | Communautaire | Moyen — 66 scripts qui appellent des API externes |

**Lacune importante :** aucun dépôt ne couvre le **droit et la fiscalité français** (micro-entreprise → SAS, holding, SCI, URSSAF, TVA, bail, BTP/décennale). Ces skills devront être écrits de zéro.

---

## 2. Organigramme proposé

```
                          ┌────────────────────────┐
                          │  TOI — Président·e      │  valide / refuse / réoriente
                          └───────────┬────────────┘
                                      │
                          ┌───────────▼────────────┐
                          │ Chief of Staff (manager)│  file d'attente des validations,
                          │ + routeur de demandes   │  points quotidiens/hebdo, relances
                          └───────────┬────────────┘
     ┌──────────────┬────────────┬────┴───────┬──────────────┬──────────────┐
 ┌───▼───┐     ┌────▼────┐  ┌────▼────┐  ┌────▼────┐   ┌─────▼────┐   ┌─────▼─────┐
 │Direction│   │Juridique│  │ Finance │  │  Tech / │   │Commercial│   │ Contrôle  │
 │stratégie│   │& sociétés│ │ & compta│  │   IT    │   │& marketing│  │ qualité   │
 └─────────┘   └─────────┘  └─────────┘  └─────────┘   └──────────┘   └───────────┘
        Appliqué à chaque entité : Micro-entreprise actuelle · future SAS · Holding ·
        Société immobilière · Créaxia · Créenovia (conception) · École
```

Principe : **aucun envoi d'e-mail, signature ou dépense sans ta validation explicite.** Le contrôle qualité relit tout livrable avant qu'il t'arrive.

---

## 3. Skills candidats par équipe

Légende recommandation : ⭐ indispensable · ✅ recommandé · ➖ optionnel

### Équipe 0 — Pilotage & coordination (le « manager »)

| # | Skill | Source | Ce qu'il apporte | Reco |
|---|---|---|---|---|
| 0.1 | `chief-of-staff` | R `c-level-advisor/skills` | Coordonne les autres rôles, prépare tes arbitrages | ⭐ |
| 0.2 | `smb-router` | K `small-business` | « Porte d'entrée » : comprend une demande floue et l'envoie au bon agent | ⭐ |
| 0.3 | `monday-brief` / `business-pulse` | K `small-business` | Point hebdo / état de santé de l'activité | ⭐ |
| 0.4 | `decision-logger` | R `c-level-advisor/skills` | Journal des décisions (qui a validé quoi, quand) | ⭐ |
| 0.5 | `task-management` + `memory-management` | K `productivity` | Liste de tâches et mémoire partagée entre sessions | ⭐ |
| 0.6 | `status-report` | K `operations` | Compte rendu d'avancement par projet | ✅ |
| 0.7 | `team-lead` + `team-communication-protocols` | W `agent-teams` | Règles de délégation entre agents | ✅ |
| 0.8 | `multi-agent-coordinator` / `task-distributor` | V `09-meta-orchestration` | Répartition du travail entre agents | ➖ |
| 0.9 | `board-meeting` / `boardroom` | R | Simulation de comité de direction sur une décision | ➖ |

### Équipe 1 — Direction & stratégie

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 1.1 | `ceo-advisor` / `founder-coach` | R | Vision, priorisation, accompagnement du fondateur | ✅ |
| 1.2 | `coo-advisor` | R | Organisation, processus | ✅ |
| 1.3 | `scenario-war-room` | R | Comparer des scénarios (ex. passage micro → SAS) | ✅ |
| 1.4 | `brainstorming` | S | Affiner une idée avant d'agir, questions une à une | ⭐ |
| 1.5 | `startup-business-analyst` | W | Business plan, étude de marché, TAM/SAM | ✅ |
| 1.6 | `project-idea-validator` / `market-researcher` | V `10-research-analysis` | Valider une idée nouvelle | ✅ |
| 1.7 | `company-os` | R | Cadre de fonctionnement d'entreprise (rituels, OKR) | ➖ |

### Équipe 2 — Juridique & structuration des sociétés

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 2.1 | `review-contract` | K `legal` | Relecture de contrats (devis, sous-traitance, bail) | ⭐ |
| 2.2 | `legal-risk-assessment` | K `legal` | Évaluer un risque juridique | ⭐ |
| 2.3 | `compliance-check` / `compliance-tracking` | K `legal` / `operations` | Suivi des obligations et échéances | ⭐ |
| 2.4 | `signature-request` | K `legal` | Circuit de validation / signature de documents | ⭐ |
| 2.5 | `triage-nda` / `vendor-check` | K `legal` | NDA et vérification fournisseurs | ✅ |
| 2.6 | `general-counsel-advisor` | R | Conseiller juridique de direction | ✅ |
| 2.7 | **À créer** : `creation-sas`, `holding-structuration`, `sci-immobilier`, `transition-micro-vers-sas` | — | Droit français — rien d'existant | ⭐ |

### Équipe 3 — Finance, comptabilité, trésorerie

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 3.1 | `cash-flow-snapshot` | K `small-business` | Trésorerie à 30/60/90 jours | ⭐ |
| 3.2 | `invoice-chase` / `pay-the-bills` | K `small-business` | Relance clients, paiement fournisseurs (avec validation) | ⭐ |
| 3.3 | `close-month` / `month-end-prep` | K `small-business` | Clôture mensuelle | ✅ |
| 3.4 | `tax-season-organizer` | K `small-business` | Préparation fiscale (à franciser) | ✅ |
| 3.5 | `cfo-advisor` | R | Directeur financier : levée, prévisionnel, rentabilité | ✅ |
| 3.6 | `variance-analysis` / `financial-statements` | K `finance` | Écarts budget / réel, états financiers | ➖ |
| 3.7 | `business-investment-advisor` | R `finance` | Analyse d'investissements (immobilier) | ✅ |
| 3.8 | **À créer** : `urssaf-micro`, `tva-btp`, `prevision-sas-is` | — | Fiscalité française | ⭐ |

### Équipe 4 — Tech / IT (compétences que tu n'as pas)

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 4.1 | `cto-advisor` | R | Choix techniques, outils, budget IT | ⭐ |
| 4.2 | `writing-plans` + `executing-plans` | S | Découper un projet tech en étapes vérifiables | ⭐ |
| 4.3 | `verification-before-completion` | S | Interdit de déclarer « fini » sans preuve | ⭐ |
| 4.4 | `system-design` / `architecture` | K `engineering` | Concevoir site, outils internes, automatisations | ✅ |
| 4.5 | `mcp-builder` | A | Connecter Claude à de nouveaux outils | ✅ |
| 4.6 | `ciso-advisor` | R | Sécurité, RGPD côté technique | ✅ |
| 4.7 | `frontend-design` / `webapp-testing` | A | Sites vitrines Créaxia / Créenovia | ➖ |

### Équipe 5 — Commercial, marketing, clients

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 5.1 | `proposal-builder` | K `small-business` | Devis / propositions commerciales | ⭐ |
| 5.2 | `inbox-manager` | K `small-business` | Tri des e-mails + brouillons de réponse | ⭐ |
| 5.3 | `crm-autopilot` / `lead-triage` | K `small-business` | Suivi prospects | ✅ |
| 5.4 | `review-reputation` | K `small-business` | Avis clients (Google…) | ✅ |
| 5.5 | `content-strategy` / `social-content-engine` | K `small-business` | Contenus réseaux sociaux | ✅ |
| 5.6 | `marketing-plan` / `copywriting` / `seo-audit` | M | Marketing approfondi | ➖ |
| 5.7 | `brand-guidelines` | A | Charte graphique par société | ➖ |

### Équipe 6 — Contrôle qualité & vérification croisée

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 6.1 | `cross-eval` | R `c-level-agents` | Un agent relit le travail d'un autre | ⭐ |
| 6.2 | `multi-reviewer-patterns` | W `agent-teams` | Relecture par plusieurs angles (juridique, chiffres, forme) | ⭐ |
| 6.3 | `verification-before-completion` | S | (voir 4.3) | ⭐ |
| 6.4 | `doc-coauthoring` | A | Relecture de documents avec le lecteur cible | ✅ |
| 6.5 | `risk-assessment` | K `operations` | Grille de risques avant validation | ✅ |

### Équipe 7 — Documents & communication (transverse)

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 7.1 | `docx` / `xlsx` / `pptx` / `pdf` | A | Produire Word, Excel, PowerPoint, PDF | ⭐ (déjà dispo dans ton Claude) |
| 7.2 | `internal-comms` | A | Comptes rendus, notes internes | ✅ (déjà dispo) |
| 7.3 | `skill-creator` | A | Outil pour écrire nos propres skills | ⭐ (déjà dispo) |

### Équipe 8 — École / formation

| # | Skill | Source | Apport | Reco |
|---|---|---|---|---|
| 8.1 | `research-analyst` / `search-specialist` | V | Recherche documentaire | ✅ |
| 8.2 | `weekly-review` / `deep-work` | R `productivity` | Organisation personnelle, révisions | ✅ |
| 8.3 | **À créer** : `suivi-ecole` (échéances, rendus, mémoire) | — | Spécifique à ton école | ⭐ |

---

## 4. Points d'alerte sécurité constatés

- **R (alirezarezvani)** : le plus riche pour la direction, mais 774 scripts et des fichiers de hooks/settings ; plusieurs mentions de contournement de permissions. → **On reprend uniquement les idées, on réécrit tout, aucun script.**
- **M (marketing)** : la majorité des scripts appellent des API externes avec des clés. → Réécriture sans scripts.
- **S (superpowers)** et **W (wshobson)** : un hook qui s'exécute au démarrage de session. → On n'installe pas de hooks tiers.
- **A** et **K** (Anthropic) : surtout du texte ; ce sont les meilleures bases.

## 5. Règles de réécriture (étape 3)

1. Uniquement des fichiers `SKILL.md` (texte) — pas de scripts tiers, pas de hooks, pas de `settings.json`.
2. Outils autorisés limités par skill (`allowed-tools`) ; aucun accès Bash pour les skills métier.
3. Toute action sortante (e-mail, partage, signature, paiement) = **brouillon + demande de validation**.
4. Rédaction en français, adaptée au droit et à la fiscalité français.
5. Chaque skill mentionne la source d'inspiration et sa licence.

## 6. Prochaine étape

Indique les numéros que tu gardes / retires (ex. « tout ⭐ + 1.3, 3.7, 5.3 ; pas d'équipe 8 pour l'instant »).
