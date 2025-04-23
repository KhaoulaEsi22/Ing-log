# OneToOneShop

**OneToOneShop** est une plateforme de commerce en ligne permettant aux utilisateurs de gérer leurs produits, commandes et paiements. Le projet suit une architecture MVC (Model-View-Controller) simple avec un backend Java, un frontend en JSP/CSS/JS, et une base de données MySQL.

## Table des matières

1. [Description du projet](#description-du-projet)
2. [Fonctionnalités principales](#fonctionnalités-principales)
3. [Technologies utilisées](#technologies-utilisées)
4. [Acteurs et rôles](#acteurs-et-rôles)
5. [Exigences fonctionnelles et non fonctionnelles](#exigences-fonctionnelles-et-non-fonctionnelles)
6. [Gestion des versions et des branches Git](#gestion-des-versions-et-des-branches-git)
7. [Intégration continue (CI/CD)](#intégration-continue-cicd)
8. [Installation et configuration](#installation-et-configuration)


## Description du projet

**OneToOneShop** est une application de commerce en ligne développée dans le cadre du cours de programmation web. Le projet comprend les fonctionnalités suivantes :

- Gestion des produits, des clients, des commandes et du panier.
- Interface administrateur pour gérer les produits, les commandes et les utilisateurs.
- Espace client pour l'inscription, la connexion, la commande et la visualisation de l'historique.
- Système de paiement et gestion de méthodes de paiement stockées en base de données.

## Fonctionnalités principales

- **Gestion des produits** : CRUD (Créer, Lire, Mettre à jour, Supprimer) des produits dans l'interface administrateur.
- **Gestion des commandes** : Consultation, création et gestion des commandes pour les utilisateurs.
- **Panier d'achat** : Ajout et suppression d'articles au panier avec gestion des sessions utilisateurs.
- **Paiement** : Choix de la méthode de paiement, enregistrée dans la base de données.
- **Interface responsive** : Utilisation de Bootstrap pour une interface adaptative et agréable.

## Technologies utilisées

- **Back-end** : Java avec Spring, servlets JSP.
- **Base de données** : MySQL pour le stockage des utilisateurs, produits, paniers et commandes.
- **Front-end** : HTML, CSS, Bootstrap, JavaScript/jQuery.
- **Contrôle de version** : Git, GitHub.
- **Outils CI/CD** : GitHub Actions ou Jenkins, Maven, JUnit, Checkstyle/PMD.
- **Autres outils** : Docker (optionnel), Nexus/Artifactory pour l'archivage des artefacts.

## Acteurs et rôles

| Acteur  | Rôle                                                     |
|---------|----------------------------------------------------------|
| Client  | Crée un compte, consulte les produits, passe des commandes |
| Admin   | Gère les produits, les clients et les commandes depuis un panel |
| Système | Gère les sessions, les interactions entre les composants |
| Base MySQL | Stocke les utilisateurs, commandes, paniers, produits |

## Exigences fonctionnelles et non fonctionnelles

### Fonctionnelles :
- Authentification client (inscription / connexion).
- Interface de gestion des produits et commandes pour l’administrateur.
- Système de panier avec session utilisateur.
- Paiement avec choix de méthode enregistrée en BDD.

### Non fonctionnelles :
- Application responsive (Bootstrap).
- Séparation logique en couches (MVC).
- Code réutilisable via beans et services.
- Base de données relationnelle avec clés primaires/étrangères.

## Gestion des versions et des branches Git

| Branche   | Description                                        |
|-----------|----------------------------------------------------|
| `main`    | Version de production                             |
| `master`  | Sauvegarde stable du projet                       |
| `develop` | Intégration des nouvelles fonctionnalités         |
| `qa`      | Tests et préproduction avant fusion vers `develop`|

GitHub est utilisé pour le suivi des versions, des pull requests, et l’intégration continue via GitHub Actions et/ou Jenkins.

## Intégration continue (CI/CD)

Le projet suit une démarche DevOps avec intégration et déploiement continus.

### Outils utilisés :
- **GitHub Actions ou Jenkins** avec Jenkinsfile.
- **Maven** pour la compilation, les tests, et le packaging.
- **JUnit** pour les tests unitaires.
- **Checkstyle / PMD** pour l’analyse statique du code.
- **JavaDoc** pour la documentation automatique.
- **Docker** (optionnel) pour le déploiement.
- **Nexus / Artifactory** pour l’archivage des artefacts.

### Workflow CI/CD :
1. Chaque push ou pull request déclenche une compilation automatique du projet.
2. Les tests unitaires sont exécutés.
3. Si tout est valide, le code est intégré dans la branche `develop` ou `main` selon le cas.

## Installation et configuration

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/username/OneToOneShop.git
   cd OneToOneShop
