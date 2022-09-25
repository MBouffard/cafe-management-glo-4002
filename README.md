# ReadMe à supprimer avant la remise

Ce readme sert à vous expliquer la structure de base de votre projet. Remplacez le avant la première remise.

## Structure

Il existe un [module maven](https://maven.apache.org/guides/mini/guide-multiple-modules.html) dans le projet :

* `cafe-api` : le projet que vous développerez. 
* Ici, vous pouvez modifier tout ce qui vous plait, tant que vous ne renommez pas les classes existantes. 
* Le code présent n'est pas nécessairement bon/bien placé/selon les normes de votre équipe. 
* À vous de voir!

## Notes sur les technologies utilisées

* [Jetty](https://www.eclipse.org/jetty/) est un Servlet Container. Il accepte les requêtes du web et sait comment répondre.
* [Jersey](https://jersey.github.io/) est un Servlet fait pour le développement d'API REST. Il sait comment faire la correspondance entre un API REST et vos méthodes selon la norme JAX-RS.
* [Jackson](https://www.baeldung.com/jackson) sert à sérialiser/désérialiser les objets JSON en POJO.

Si vous n'êtes pas familiers avec ces concepts, il est fortement suggéré d'utiliser google/stackoverflow pour les apprendre rapidement. 
Ceux-ci peuvent être matière à examen.

:warning: Jetty, Jersey et Jackson sont utilisés dans le projet de base.
Vous pouvez choisir d'autres technologies, mais vous devrez analyser les avantages et inconvéniants d'abord. 
Si vous voulez le faire, venez nous en parler. 
Entre autre, Spring et Spring Boot sont reconnus pour causer des maux de têtes vers la fin de la session. 
Dans le passé, certains étudiants ont râtés certaines remises à cause de ce choix.

## Intégration Docker

Un Dockerfile est également fournis si vous désirez essayer de rouler votre code sur les mêmes images docker que nous utiliserons.

Pour ce faire:

```bash
docker build -t application-glo4002 .
docker run -p 8181:8181 application-glo4002
```

## Démarrer le projet

Vous pouvez démarrer le serveur (CafeServer).

Le `main()` ne demande pas d'argument.

Vous pouvez également rouler le serveur via maven (**c'est ce qui sera utilisé pour corriger votre projet**) :

```bash
mvn clean install
mvn exec:java -pl cafe-api
```

:warning: Ces commandes seront utilisées pour la correction automatique du projet. Elles doivent donc fonctionner!

Une resource "heartbeat" vous est fournis pour tester que le service démarre bien. 
Allez à l'URL `http://localhost:8181/heartbeat?token=unique_token` pour le valider. 
Vous n'êtes pas obligés de garder le heartbeat (mais si vous le supprimez, ne laissez pas de code mort!)

## Prochaines étapes

Nous regarderons le projet ensemble pendant les premières séances du cours. 
Le client sera également présent pour vous le présenter davantage. 
D'ici là, assurez-vous de pouvoir exécuter le code sur votre machine.

## Besoin d'aide?

Contactez-nous sur Discord à partir de votre channel d'équipe si quelque chose ne fonctionne pas!
