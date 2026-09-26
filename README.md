# Introduction étape par étape au framework web [Spring MVC]

**Le cours : https://stahe.github.io/springmvc-sept-2026/**

Auteur de la totalité des codes et du cours : **Claude** (IA d'Anthropic) sur demande de **Serge Tahé**— septembre 2026.

## Présentation

Ce cours enseigne, pas à pas, la construction d'applications web avec **Spring MVC** (Spring Boot 4), où c'est le serveur qui fabrique les pages HTML (vues **Thymeleaf**). Il ne suppose connues que les bases de HTTP, de HTML et du langage Java.

Il se compose de deux parties :

- **28 petits exemples**, chacun centré sur une notion, regroupés en chapitres :

| Chapitre | Contenu | Exemples |
|---|---|---|
| Contrôleurs, actions, routage | du navigateur à l'action : routes, réponses, redirections, services et injection de dépendances | 01 à 06 |
| Le modèle d'une action | paramètres de la requête : liaison, conversion, validation, requêtes POST, liaison personnalisée | 07 à 12 |
| La vue et son modèle | Thymeleaf, gabarit et fragments, helpers, formulaires, validation, Post / Redirect / Get | 13 à 21 |
| Internationalisation | une application en deux langues (MessageSource, LocaleResolver) | 22 |
| Portées des données | beans singleton, requête, prototype ; cookies | 23 |
| Le cycle de vie d'une requête | filtres de servlet, intercepteurs, `@ControllerAdvice`, page d'erreur | 24 |
| Authentification et autorisation | Spring Security, jeton JWT dans un cookie, rôles, captcha, limitation des tentatives | 25 à 27 |
| Architecture en couches et accès aux données | couches web / métier / DAO, Spring Data JPA, Hibernate, MySQL, transactions | 28 |

- **une étude de cas complète**, l'application **RdvMedecins** de prise de rendez-vous pour un cabinet médical : trois rôles (administrateur, médecins, patients), agenda, réservation et annulation, gestion des médecins et des clients, création de compte par le patient, protection contre les robots, interface en français et en anglais. Chacun de ses fichiers est commenté dans le cours.

## Les codes

Les codes sont téléchargeables depuis le cours. Ils comprennent :

- `exemples/` : les 28 exemples, un module Maven par dossier ;
- `rdvmedecins2-spring-mvc/` : l'étude de cas.

## Technologies

Java 21 · Spring Boot 4.1 (Spring MVC, Spring Security, Spring Data JPA) · Thymeleaf · Hibernate · MySQL 8 (ou MariaDB) · Maven (Maven Wrapper) · Bootstrap 5.

## Prérequis

- un JDK 21 (par exemple Eclipse Temurin) ;
- Visual Studio Code, avec les extensions « Extension Pack for Java » et « Spring Boot Extension Pack » ;
- MySQL 8 (Laragon sous Windows) ou MariaDB, pour l'exemple 28 et l'étude de cas ;
- curl.

L'installation de ces outils est décrite dans les annexes du cours.

## Lancer un exemple ou l'étude de cas

```bash
# un exemple (port 5000), depuis son dossier
cd exemples/01-structure
../mvnw spring-boot:run          # Windows : ..\mvnw spring-boot:run

# l'étude de cas (port 8081), après avoir créé la base avec database/dbrdvmedecins2.sql
cd rdvmedecins2-spring-mvc
./mvnw spring-boot:run           # Windows : mvnw spring-boot:run
```

Au premier lancement, le Maven Wrapper télécharge Maven puis les bibliothèques : il faut être connecté à Internet.
