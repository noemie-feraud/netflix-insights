#Netflix Data Analysis - Insights & Trends

Ce projet analyse le catalogue de films et séries disponibles sur Netflix (jusqu'en 2021). 
L'objectif est d'explorer la répartition des contenus, d'identifier les tendances de production par pays et de nettoyer les données pour en extraire des statistiques exploitables.

#Fonctionnalités du projet
* **Nettoyage de données** : Conversion des dates, traitement des valeurs manquantes et normalisation des durées.
* **Analyse Descriptive** : Identification des années records pour les ajouts de contenus.
* **Visualisation** : 
    * Graphique de répartition Films vs Séries.
    * Top 10 des pays producteurs.
    * Top 10 des genres les plus populaires.

#Outils utilisés
* **Python 3.12**
* **Pandas** : Pour la manipulation des données.
* **Matplotlib & Seaborn** : Pour les visualisations graphiques.
* **Missingno** : Pour l'audit des données manquantes.

#Structure des fichiers
* `Netflix Data Analysis.ipynb` : Le notebook contenant tout le code et l'analyse.
* `netflix_titles.csv` : Le dataset d'origine.
