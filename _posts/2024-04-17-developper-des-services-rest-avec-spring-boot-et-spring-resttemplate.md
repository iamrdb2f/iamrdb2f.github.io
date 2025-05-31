---
layout: post
title: "Comment développer des services Rest avec Spring Boot et Sprint RestTemplate"
categories: Programmation
author:
- Roland Guissony
---

Dans ce tutoriel, qui risque d'être long, nous allons voir comment développer des services Rest avec Spring Boot et Spring RestTemplate. Le client et le serveur seront développés dans deux applications distinctes.

Je précise d'entrée de jeu que ce texte et l'ensemble des exercises proposés ici, sont inspirés du livre de Bertrand Nguimgo, que je remercie pour la qualité de son travail.

# Développement du serveur avec Spring Boot

Tout d'abord, nous allons créer un projet Spring Boot. Pour cela, nous allons utiliser l'outil Spring Initializr. Pour cela, rendez-vous sur le site [https://start.spring.io/](https://start.spring.io/). 

![Spring Initializr](https://media.geeksforgeeks.org/wp-content/uploads/20231102130522/Spring_initializr.png)

Voici le code contenu dans la classe SpringbootRestserverapiApplication.java :

```java
package org.ucollective.springbootrestserverapi;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SpringbootRestserverapiApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringbootRestserverapiApplication.class, args);
	}

}
```

Voici la classe ServletInitializer.java : 
  
  ```java
package org.ucollective.springbootrestserverapi;

import org.springframework.boot.builder.SpringApplicationBuilder;
import org.springframework.boot.web.servlet.support.SpringBootServletInitializer;

public class ServletInitializer extends SpringBootServletInitializer {

	@Override
	protected SpringApplicationBuilder configure(SpringApplicationBuilder application) {
		return application.sources(SpringbootRestserverapiApplication.class);
	}

}
```
La classe RestServices.java contient le code suivant :

```java
package org.ucollective.springbootrestserverapi;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class RestServices {
    private static final Logger logger = LoggerFactory.getLogger(RestServices.class);

    @GetMapping(value = "/")
    public ResponseEntity<String> pong(){
        logger.info("Démarrage des services OK .....");
        return new ResponseEntity<String>("Réponse du serveur: "+ HttpStatus.OK.name(), HttpStatus.OK);
    }

}
```

