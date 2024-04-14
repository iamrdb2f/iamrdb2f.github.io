---
layout: post
title: "Un Framework de tests automatisé basé sur Selenium et utilisant Orange Human Ressources Management (OHRM)"
categories: Programmation
author:
- Roland Guissony
---

![Logo de Selenium](https://www.all4test.fr/wp-content/uploads/2023/12/selenium.jpeg)

Orange HRM est un logiciel de gestion des ressources humaines open source. Il est utilisé par de nombreuses entreprises pour gérer leurs ressources humaines. Il est basé sur Java et utilise une base de données MySQL. Il est également compatible avec les navigateurs Web les plus populaires tels que Chrome, Firefox, Safari et Internet Explorer.

## Introduction
Dans ce tutoriel, nous allons créer un framework de test automatisé basé sur Selenium et utilisant Orange HRM. Nous allons utiliser Java comme langage de programmation et Maven comme gestionnaire de dépendances. Nous allons également utiliser TestNG comme framework de test. Cet article montre comment créer et configurer le projet de base. Un article avenir traitera de l'automatisation de différents scénarios de test à proprement parler.

## Création du projet avec Spring Initializr
Pour créer le projet, allez sur le site [Spring Initializr](https://start.spring.io/) et configurez les dépendances suivantes :

- Sélectionnez Maven Project comme type de projet.
- Sélectionnez Java comme langage de programmation.
- Sélectionnez la version de Java que vous souhaitez utiliser.
- Ajoutez les dépendances suivantes :
  - Selenium
  - TestNG
  - Lombok
  - Log4j2
  - Spring Boot DevTools
  - Spring Web
  - Spring Boot Starter Test
  - allure-testng
  - allure-spring-boot-starter
  - poi-ooxml
  - poi
  - poi-ooxml-schemas
  - selenium-java
- Nommer votre projet : `OrangeHRMTestAutomation`, choisir le nom de votre package, ajoutez une description et cliquez sur le bouton Generate.

## Configuration du projet
Après avoir généré le projet, importez-le dans votre IDE préféré.

Une fois le projet importé, ouvrez le fichier `pom.xml`, copiez et coller le code contenu dans le fichier `pom.xml` du projet dans le Repository Github suivant : [Un Framework de tests automatisé basé sur Selenium et utilisant Orange Human Ressources Management (OHRM)](https://github.com/iamrdb2f/orangehrm-test-aut-framework).

Vous pouvez maintenant ajouter les packages suivants à votre projet :

- `config` : contient les classes de configuration.
- `pages` : contient les classes de page.
- `tests` : contient les classes de test.
- `utils` : contient les classes utilitaires.
- `handlers` : contient les classes de gestion des événements.
- `listeners` : contient les classes d'écouteurs.
- `extentreports` : contient les rapports d'exécution.
- `resources` : contient les fichiers de configuration.

Veillez bien à ce que le répertoire resources soit marqué comme **Test Resources Root**.

Pour poursuivre la suite de ce projet, veuillez consulter le Repo Github suivant afin d'adapter la structure de votre projet : [Un Framework de tests automatisé basé sur Selenium et utilisant Orange Human Ressources Management (OHRM)](https://github.com/iamrdb2f/orangehrm-test-aut-framework)

Pour aller plus loin et collaborer avec moi dans le cadre de ce projet, veuillez me contacter à l'adresse mail suivante : [dev@rolandguissony.com](mailto:dev@rolandguissony.com) afin de demander un accès au projet et à l'équipe principale.
