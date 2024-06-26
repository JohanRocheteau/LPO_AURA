# Projet Bénévolat : LPO-AURA
![Logo](Photos/Logo.jpg)

## Mise en situation :
- **But :** Récupération automatique, via une API, des données issues d’une sonde météorologique et stockage en PostgreSQL. 
- **Problématique :** Actuellement les données sont récupérées tous les X jours  sous format CSV et transférées manuellement sur PostgreSQL. Ces étapes sont réalisées par plusieurs personnes et nécessites de supprimer les doublons. 
- **API :** [API WEATHERLINK](https://weatherlink.github.io/v2-api/)
- **Contraintes :** En plus des clés pour l’utilisation de l’API et de la BDD il faut gérer le fait que l’API ne permet de récupérer les données que un jour à la fois, pour une sonde qui remonte à fin septembre 2021.

## Réalisations :
- **Librairies principales :** requests, datetime,  psycopg2, dotenv, sqlalchemy
- **Détails du projet :**
	- Création d’un environnement virtuel via Poetry.
	- Création d’un fichier contenant les secrets (clés et mdp).
	- Création de trois fichiers notebooks et scripts python permettant la récupération et le stockage des données sur PostgreSQL :
		- un pour la partie historique
		- un pour la récupération des nouvelles données
		- et finalement un regroupant les deux premiers.
	- Ajout des librairies black, isort, flake8 & flake8-isort, pylint et pre-commit pour la vérification de la qualité du code python envoyé sur GutHub.
 	- Transformation des scripts avec la librairie python "click" afin de créer une petite application en invite de commande. 
