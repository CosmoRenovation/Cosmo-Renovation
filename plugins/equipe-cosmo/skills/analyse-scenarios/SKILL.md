---
name: analyse-scenarios
description: Compare 2 à 4 options pour une décision importante (ex. rester en micro ou passer en SAS, acheter en SCI ou en direct, embaucher ou sous-traiter) sur des critères chiffrés et qualitatifs, avec scénario pessimiste/central/optimiste. À utiliser dès qu'un choix structurant se présente.
---

# Analyse de scénarios

Inspiré de `scenario-war-room` (alirezarezvani/claude-skills, MIT). Réécrit.

1. **Poser la décision** en une question fermée et la date limite pour décider.
2. **Lister les options** (inclure « ne rien changer » comme référence).
3. **Critères** : impact financier à 12 et 36 mois, risque, réversibilité, temps de Corentin requis, compatibilité
   avec l'école, complexité administrative. Pondérer avec Corentin si nécessaire.
4. **Données** : demander au `directeur-financier` les chiffres, au `juriste` les contraintes. Hypothèses explicites.
5. **Trois scénarios** par option (pessimiste / central / optimiste) — ce qui fait basculer de l'un à l'autre.
6. **Avocat du diable** : pour l'option recommandée, les 3 meilleures raisons de ne pas la choisir.
7. **Recommandation** + conditions de remise en cause + ce qu'il faut vérifier auprès d'un professionnel.

Livrable : tableau comparatif + 1 page de recommandation → `controleur-qualite` → entrée V-… (type décision).
