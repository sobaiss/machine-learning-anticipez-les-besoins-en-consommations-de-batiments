# Anticipez les besoins en consommations de bâtiments

Ce projet analyse la consommation énergétique des bâtiments non résidentiels et construit des modèles de régression pour prédire :

- `SiteEnergyUse(kBtu)` la consommation d'énergie des batiments
- `TotalGHGEmissions` les émissions de gaz des bâtiments

## Fichier principal

Le script principal du projet est le notebook :

- `P3_template_modelistation_supervisee_data_scientist.ipynb`

Ce notebook contient :
- l’analyse exploratoire des données,
- le feature engineering,
- la préparation des données pour la modélisation,
- la comparaison de plusieurs modèles supervisés,
- l’optimisation d’un `RandomForestRegressor`,
- l’interprétation des résultats.

## Données

Les données sources se trouvent dans :

- `data/2016_Building_Energy_Benchmarking.csv`

Le notebook génère également ces fichiers de sortie :

- `data/filtered_non_residential_buildings.csv`
- `data/featured_non_residential_buildings.csv`

## Structure du projet

- `P3_template_modelistation_supervisee_data_scientist.ipynb` : Notebook principal du projet
- `README.md` : Documentation du projet
- `pyproject.toml` : Métadonnées du projet Python
- `data/` : Dossier contenant les jeux de données CSV

## Installation et exécution

1. Ouvrir le notebook dans Jupyter Notebook ou JupyterLab.
2. Exécuter les cellules dans l’ordre :
   - import des bibliothèques
   - chargement du dataset
   - nettoyage et filtrage
   - analyse exploratoire
   - modélisation et évaluation

## Objectifs

- Comprendre les déterminants de la consommation énergétique des bâtiments
- Créer un pipeline de modélisation supervisée
- Évaluer plusieurs modèles de régression
- Optimiser un modèle pour limiter le surapprentissage

## Notes

- Le notebook se concentre sur les bâtiments non résidentiels.
- Les colonnes contenant des informations d’identification ou des fuites de données sont supprimées avant la modélisation.
- Les variables cibles sont transformées avec `log(1 + x)` pour stabiliser la distribution.
