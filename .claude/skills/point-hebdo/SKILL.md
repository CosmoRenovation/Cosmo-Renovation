---
name: point-hebdo
description: Bilan hebdomadaire par entité (avancées, chiffres clés, décisions prises, risques, priorités de la semaine suivante) préparé par le Chef de cabinet avec les agents. À utiliser quand Corentin tape /point-hebdo, en fin ou début de semaine, ou lors d'une exécution planifiée hebdomadaire.
---

# Point hebdo

## Déroulé
1. Pour chaque entité active, demander en parallèle aux agents concernés un statut en 5 lignes max
   (financier : trésorerie et factures ; commercial : devis et prospects ; juriste : échéances et risques ;
   technique : outils et incidents ; école : rendus à venir).
2. Lister les décisions inscrites cette semaine (journal) et les validations encore en attente.
3. `controleur-qualite` relit la synthèse (cohérence des chiffres, oublis).
4. Proposer **3 priorités** pour la semaine suivante, chacune avec entité, responsable, résultat attendu.

## Format
Un bloc par entité (🟢 en route / 🟡 attention / 🔴 problème), puis « Décisions de la semaine », « En attente de toi »,
« Priorités proposées » (à valider : créer une entrée V-… de type décision).
Enregistrer dans `bureau/rapports/AAAA-MM-JJ-point-hebdo.md`.
