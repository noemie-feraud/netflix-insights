# Netflix Data Analysis — Insights & Trends

---

## Table des matières

1. [AI Watch — Veille sur l'intelligence artificielle](#1-ai-watch--veille-sur-lintelligence-artificielle)
2. [Contexte du projet et données utilisées](#2-contexte-du-projet-et-données-utilisées)
3. [Observations et conclusions](#3-observations-et-conclusions)

---

## 1. AI Watch — Veille sur l'intelligence artificielle

### L'intelligence artificielle

L'intelligence artificielle (IA) désigne l'ensemble des techniques permettant à des machines de simuler des capacités cognitives humaines : comprendre, raisonner, apprendre et prendre des décisions. Elle repose sur des algorithmes capables de traiter de grandes quantités de données pour résoudre des problèmes ou automatiser des tâches.

### Le Machine Learning

Le Machine Learning, ou apprentissage automatique, est une branche de l'IA dans laquelle on ne programme pas explicitement les règles : on fournit des données à un algorithme qui apprend par lui-même à identifier des patterns et à faire des prédictions. Plus le modèle reçoit de données, plus il s'améliore.

### Le pré-traitement des données

Le pré-traitement des données est l'étape de préparation qui précède toute analyse ou tout entraînement de modèle. On y nettoie les données brutes : gestion des valeurs manquantes, suppression des doublons, conversion des types, normalisation des formats. C'est une étape essentielle car la qualité des résultats dépend directement de la qualité des données en entrée.

### L'analyse descriptive des données

L'analyse descriptive consiste à explorer un jeu de données pour en comprendre la structure, les tendances et les distributions. On utilise des statistiques simples (moyennes, médianes, fréquences) et des visualisations (graphiques, histogrammes) pour résumer l'information et en tirer des premières observations. C'est la fondation de toute démarche de data science.

### Application de l'IA dans le marketing

On a choisi le domaine du marketing, car c'est probablement celui où l'on croise l'IA le plus souvent dans notre quotidien, sans forcément s'en rendre compte.

* **Personnalisation des recommandations.** 
Quand Netflix nous suggère une série, quand Spotify crée une playlist "Découvertes de la semaine" ou quand un site e-commerce nous affiche "vous aimerez aussi", c'est de l'IA. Les algorithmes analysent notre historique de navigation, nos achats et nos clics pour nous proposer du contenu adapté à nos goûts. Le but est de nous garder engagés le plus longtemps possible et de nous montrer les bons produits au bon moment.

* **Analyse prédictive.** 
L'IA permet aux entreprises d'anticiper les comportements des consommateurs avant même qu'ils n'agissent. Par exemple, un site peut détecter qu'un client est sur le point d'abandonner son panier et lui envoyer automatiquement une promotion ciblée pour le convaincre de finaliser son achat. Les marques peuvent aussi prévoir quels produits vont bien se vendre selon la saison, la tendance ou le profil du client.

* **Automatisation des campagnes.** 
Grâce à l'IA, les entreprises peuvent gérer leurs publicités à grande échelle sans intervention humaine constante. Les algorithmes ajustent en temps réel les messages publicitaires, choisissent les meilleures plateformes pour diffuser une annonce et adaptent le budget en fonction des résultats. Ce qui prenait des jours à une équipe marketing peut maintenant être fait automatiquement en quelques secondes.

**Chatbots et relation client.** 
Les assistants virtuels alimentés par l'IA sont capables de répondre aux questions des clients à toute heure, de les guider dans un processus d'achat ou de gérer le service après-vente. Cela permet aux entreprises de rester disponibles en permanence sans mobiliser une équipe humaine.

**Les limites éthiques.** Toutes ces capacités soulèvent des questions importantes. La frontière entre personnalisation utile et manipulation est fine : quand un algorithme exploite nos biais cognitifs pour nous pousser à acheter quelque chose dont on n'a pas besoin, on passe de l'aide à la manipulation. La collecte massive de données personnelles et le manque de transparence sur le fonctionnement des algorithmes posent aussi de vrais enjeux de vie privée et de confiance.

---

## 2. Contexte du projet et données utilisées

### Objectif

On a réalisé une analyse exploratoire du catalogue Netflix à partir d'un dataset contenant les films et séries TV disponibles sur la plateforme jusqu'en septembre 2021. Notre objectif était de nettoyer ces données, d'en comprendre la structure et d'en extraire des tendances à travers des visualisations.

### Données utilisées

Le dataset `netflix_titles.csv` contient 8807 entrées et 12 variables : `show_id` (identifiant unique), `type` (film ou série), `title`, `director`, `cast`, `country`, `date_added` (date d'ajout au catalogue), `release_year`, `rating` (classification d'âge), `duration`, `listed_in` (genres) et `description`.

### Outils utilisés

On a travaillé avec **Python 3** dans un **Jupyter Notebook**, en utilisant Pandas pour la manipulation des données, Matplotlib et Seaborn pour les visualisations, et Missingno pour l'audit des valeurs manquantes.

### Structure des fichiers

- `Netflix Data Analysis.ipynb` : le notebook Jupyter contenant tout le code, l'analyse et les visualisations.
- `netflix_titles.csv` : le dataset d'origine (8807 entrées, 12 colonnes).
- `README.md` : ce fichier.

---

## 3. Observations et conclusions

### Répartition du contenu

On observe que le catalogue Netflix est largement dominé par les films, qui représentent environ **69,6%** du contenu total, contre **30,4%** pour les séries TV. Netflix mise donc davantage sur la quantité de films, bien que les séries génèrent souvent plus d'engagement.

### Tendances géographiques

Les **États-Unis** dominent massivement la production de contenu présent sur Netflix, loin devant l'Inde qui occupe la deuxième place. Le Royaume-Uni, le Canada et la France figurent également dans le top 10. On constate que Netflix a une stratégie résolument internationale, avec du contenu issu de dizaines de pays différents.

### Évolution temporelle des ajouts

Le nombre de contenus ajoutés au catalogue a connu une **croissance exponentielle** entre 2015 et 2019, avec un pic marqué en 2019. 
On note un ralentissement en 2020 et 2021, probablement lié aux perturbations de production causées par la pandémie de COVID-19. Avant 2015, les ajouts étaient très limités, ce qui reflète la transition de Netflix vers le streaming.

### Ratings

Les classifications les plus fréquentes sont **TV-MA** (contenu mature) et **TV-14**, ce qui montre que Netflix cible principalement un public adulte. Les contenus destinés aux enfants (TV-Y, TV-G) sont nettement moins représentés. 
On a également repéré des anomalies dans les données : certaines valeurs de la colonne `rating` contenaient des durées ("74 min", "84 min") au lieu de classifications, ce qu'on a nettoyé.

### Durée des contenus

La majorité des films durent entre 80 et 120 minutes, avec une distribution **centrée autour de 100 minutes**. 
Côté séries, on observe que la grande majorité ne comptent qu'une seule saison. Cela reflète la tendance aux **mini-séries** et aux **séries limitées**, ainsi que le grand nombre de séries annulées après une première saison.

### Genres populaires

Les genres les plus représentés sont **les drames internationaux**, **les comédies internationales** et **les documentaires**. 
On remarque la prédominance du tag "International" dans les genres les plus fréquents, ce qui confirme la volonté de Netflix de se positionner comme une plateforme globale avec un contenu diversifié.

### Réalisateurs

On a identifié de nombreux réalisateurs ayant produit plusieurs œuvres pour Netflix. Les plus prolifiques viennent souvent d'Inde, ce qui est cohérent avec le volume important de contenu indien sur la plateforme. 
Pour les œuvres françaises spécifiquement, on observe une répartition plus éclatée avec peu de réalisateurs dominant clairement.

### Qualité des données

L'audit des données manquantes a révélé que la colonne `director` est incomplète à environ 30%, suivie par `cast` et `country`. 
Ces lacunes limitent certaines analyses mais n'empêchent pas de dégager des tendances globales fiables.

### Conclusion générale

À travers cette analyse, on constate que Netflix a massivement investi dans l'expansion de son catalogue entre 2015 et 2020, avec une stratégie claire d'internationalisation du contenu. 
La plateforme vise principalement un public adulte tout en maintenant une offre diversifiée en termes de genres, de durées et d'origines géographiques. 
Le ralentissement observé en 2020-2021 semble conjoncturel plutôt que structurel, lié au contexte sanitaire mondial.

## [![Réalisé par](https://img.shields.io/badge/R%C3%89ALIS%C3%89-PAR-orange?style=for-the-badge)](https://forthebadge.com)

**Hiba TRABELSI** | **Jean-Pierre GUIRADO** | **Noémie FERAUD**