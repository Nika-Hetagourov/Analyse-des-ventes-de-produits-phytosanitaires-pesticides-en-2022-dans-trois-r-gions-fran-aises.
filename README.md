## Projet d’Économétrie (L3) — Analyse des ventes de pesticides (2022)

### Contexte et objectif
Ce projet analyse les **ventes de produits phytosanitaires (pesticides) en 2022** dans trois régions :
- **Normandie**
- **Guadeloupe**
- **Auvergne-Rhône-Alpes**

L’objectif est de comprendre **ce qui explique les différences de quantités achetées** selon :
- la **région**
- le **type / classification de danger** des substances

### Structure du fichier `Rmd`
Le fichier `projet_final_L3_econometrie_complet.Rmd` contient :
- une **introduction** avec la problématique
- une **description des données** (variables, types, nature)
- des **statistiques descriptives** + graphiques
- **3 modèles économétriques** expliquant les quantités achetées
- des **tests statistiques** (Student, Fisher, Breusch-Pagan, ANOVA…)
- une étape de **fusion de données entre régions**
- une **conclusion** avec limites

### Données (résumé simple)
- Chaque ligne correspond à un **achat de produit/substance** dans un **code postal**
- Variables principales : **quantité achetée**, **catégorie de danger**, **région**, etc.
- Données en **coupe transversale** (une seule année : 2022)

### Analyse statistique
- moyennes, médianes, écarts-types des quantités
- graphiques sur la répartition des classes de danger
- comparaisons entre régions (ex : Normandie vs Guadeloupe)

### Modèles économétriques
Les régressions utilisent une **régression linéaire (MCO)** sur le **logarithme des quantités**.

- **Modèle 1** : effet de la **région** (Normandie vs Guadeloupe)
- **Modèle 2** : effet de la **classification de la substance** + région
- **Modèle 3** : modèle complet (3 régions + classifications)

Chaque modèle est interprété via :
- coefficients estimés
- significativité des coefficients
- tests associés

### Tests statistiques utilisés
- **Student** : significativité des coefficients
- **Fisher** : significativité globale du modèle
- **Breusch-Pagan** : hétéroscédasticité (homogénéité des erreurs)
- **ANOVA** : comparaison de modèles / effets

### Fusion des données (cas Auvergne-Rhône-Alpes)
La base Auvergne-Rhône-Alpes étant incomplète, elle est **fusionnée avec Normandie** pour :
- associer chaque produit à ses substances
- répartir la quantité du produit entre substances (au prorata)

### Conclusion (résumé)
- des **différences entre régions** existent
- les substances **CMR** ou **dangereuses pour l’environnement** sont plus utilisées
- une partie importante des différences reste inexpliquée (variables manquantes : surface agricole, types de cultures, etc.)
