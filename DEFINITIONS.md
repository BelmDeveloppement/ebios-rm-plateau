# Fiche de définitions · Opération EBIOS RM

Un seul vocabulaire pour toute la table. La colonne « Où le trouver » indique la carte ou la zone du plateau qui porte la notion.

## Pour tous

| Terme | Définition | Où le trouver |
|---|---|---|
| **Valeur métier (VM)** | Ce qui est essentiel à la mission de l'organisation (un processus, une information, un savoir-faire). Test : « si on change de technologie, cela existe-t-il encore ? » | Carte bleue ENTREPRISE |
| **Bien support (BS)** | Composante du SI, de l'OT, des locaux ou des personnes sur laquelle repose une valeur métier. Il disparaît avec la technologie. | Carte bleue ENTREPRISE |
| **Événement redouté (ER)** | Atteinte à une valeur métier selon un critère (disponibilité, intégrité, confidentialité), avec son impact. On ne décrit jamais l'attaque. | Carte bleue ENTREPRISE |
| **Gravité (G1 à G4)** | Niveau d'impact d'un ER, coté avec l'échelle du dossier de scénario (calcul jours d'arrêt × coût par jour quand c'est possible). Un ER qui touche la sécurité des personnes est G4. | Dossier de scénario ; feuille 1 |
| **Vraisemblance (V1 à V4)** | Facilité avec laquelle un scénario peut se produire. Cotée par critères à l'atelier 3, par étapes à l'atelier 4. | Feuilles 3 et 2 |
| **Risque** | Gravité × vraisemblance (G × V). Faible ≤ 3 · Moyen 4 à 6 · Élevé 8 à 9 · Critique ≥ 12. | Matrice atelier 5 |

## Atelier 1 · Cadrage et socle

| Terme | Définition | Où le trouver |
|---|---|---|
| **Socle de sécurité** | 8 règles de base. Chacune est notée Conforme (1 point), Partielle (0,5) ou Écart (0). Taux de conformité = points ÷ 8. | Feuille 1 ; constats d'audit du dossier |

## Atelier 2 · Sources de risque

| Terme | Définition | Où le trouver |
|---|---|---|
| **Source de risque (SR)** | Personne ou groupe qui peut porter atteinte à l'organisation : État, cybercriminel, hacktiviste, concurrent, initié, amateur… | Carte rouge MENACE |
| **Objectif visé (OV)** | Ce que la source cherche à obtenir (espionnage, gain financier, vengeance, défi). Ce n'est pas un ER : l'objectif est ce que veut l'attaquant, l'ER est ce que redoute l'entreprise. | Carte rouge MENACE |
| **M, R, A et pertinence (Σ)** | Motivation, Ressources, Activité, chacune de 1 à 4. Σ = M + R + A : ≥ 8 retenu · 6 à 7 à surveiller · ≤ 5 écarté. | Feuille 2 |
| **Couple retenu** | Couple source / objectif dont Σ ≥ 8. Seul un couple retenu compte dans le contrôle de couverture. | Feuille 2 |
| **Couverture** | Contrôle de cohérence : chaque ER de gravité G3 ou G4 doit être atteint par au moins un couple retenu. Sinon la sélection est trop restrictive. Une source à surveiller ou écartée ne couvre rien. | Feuille 2, bas |

## Atelier 3 · Écosystème et scénarios stratégiques

| Terme | Définition | Où le trouver |
|---|---|---|
| **Partie prenante (PP)** | Entité extérieure en relation avec l'organisation (fournisseur, prestataire, partenaire). Elle peut servir de rebond. | Carte verte ÉCOSYSTÈME |
| **D, P, M, C** | Dépendance et Pénétration font monter la menace ; Maturité cyber et Confiance la font baisser. Valeurs de 1 à 4 imprimées sur la carte. | Carte verte ÉCOSYSTÈME |
| **Niveau de menace** | (D × P) ÷ (M × C). Danger ≥ 3 · Contrôle de 1,5 à moins de 3 · Veille moins de 1,5. | Radar, feuille 3 |
| **Scénario stratégique (SS)** | Chemin d'attaque source de risque → partie prenante (relais) → événement redouté. Sa gravité est celle de l'ER. On pose 3 cartes dans le couloir ; le second emplacement PP reste vide sauf second relais justifié. | Couloir SS du plateau |
| **Critères A, B, C** | A : Σ de la source ≥ 9. B : la PP du chemin est en zone danger. C : une règle du socle sur le chemin est en Écart ou Partielle. V = nombre de critères remplis (minimum V1, maximum V3). | Feuilles 1, 2 et 3 |
| **Mesure d'écosystème (ME)** | Action sur une partie prenante qui change UNE variable de 1 (D ou P : −1 · M ou C : +1). Elle a un coût en jetons, repris sur le budget de l'atelier 5. | Carte vert foncé MESURE ÉCOSYSTÈME |

## Atelier 4 · Scénarios opérationnels

| Terme | Définition | Où le trouver |
|---|---|---|
| **Scénario opérationnel** | Enchaînement de 4 actions sur des biens supports : Connaître, Rentrer, Trouver, Exploiter (CRTE). | Cartes noires OPÉRATION |
| **Tests T1 à T4** | Pour écarter une action : bien connu (T1), valeur métier (T2), chemin vers un ER (T3), enchaînement (T4). Trois cartes sont hors sujet. | Feuille 2 |
| **Freins F1 à F4** | Chaque frein fait baisser la vraisemblance d'une étape : V étape = 4 − nombre de freins (minimum 1). V du scénario = la plus faible des 4 étapes. | Feuille 2 |
| **Bien support critique** | Bien visé par au moins 2 des 12 actions posées, dont au moins un Rentrer ou un Exploiter. | Feuille 2 |

## Atelier 5 · Traitement du risque

| Terme | Définition | Où le trouver |
|---|---|---|
| **Mesure du plan** | Action de sécurité qui réduit G ou V. Elle coûte des jetons ; le budget total est de 14 jetons. | Carte orange MESURE |
| **Seuil d'acceptation** | Niveau de risque que la direction accepte : G × V ≤ 6. Au-dessus, le scénario doit être traité (mesure en plus) ou faire l'objet d'une dérogation signée du DG. | Matrice, feuille 4 |
| **Risque résiduel** | Risque qui reste après traitement. Il est accepté formellement : responsable du suivi, indicateur, date de revue. | Feuille 4 |
| **Veto sécurité** | Le responsable de la sécurité des personnes peut s'opposer à l'acceptation d'un risque qui touche l'ER de sécurité. | Carte jaune RÔLE ; feuille 4 |
| **Stratégies de traitement** | Réduire, éviter, partager (assurance : ne change ni G ni V) ou accepter. | Cartes orange MESURE |
| **PACS** | Plan d'amélioration continue de la sécurité : mesures, responsables, échéances. | Zone PACS du plateau |

## Cartes de jeu

| Terme | Définition | Où le trouver |
|---|---|---|
| **Carte Aléa** | Événement lu par l'animateur à mi-parcours : il oblige à recoter. La version 1 n'est jamais effacée. | Carte violette ALÉA |
| **Carte Rôle** | Votre point de vue, vos questions et votre position à défendre. À ne pas montrer aux autres. | Carte jaune RÔLE ; fiche de rôle |
