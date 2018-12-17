![Puzzle ITC Logo](../assets/reveal.js-3.6.0/lib/img/puzzle_tagline_bg_rgb.svg)
<!-- .slide: class="master01" -->


<!-- slide -->
<!-- .slide: class="master02" -->
### JHipster
Adrian Bader<br>
Sombra González


<!-- slide -->
<!-- .slide: class="master03" -->
### Was ist JHipster

JHipster ist ein Werkzeug,
um Web-Applikationen mit <br>
Spring Boot und<br>
Angular oder React zu generieren

![](../assets/img/jhipster/jhipster.png)

<!-- slide -->
<!-- .slide: class="master03" -->
### Wieso JHipster

* MVP-Erstellung für B4U
* Marina
* Energy-Kitchen


<!-- section -->
<!-- .slide: class="master04" -->
### Applikationenarten

* Monolithic application
* Microservice 
    * Microservice application: Services
    * Microservice gateway: Edge server
    * Hipster UAA server: OAuth2 authentication server

<!-- slide -->
<!-- .slide: class="master03" -->
### Client-side Technologien

* Angular / React
* Bootstrap
* HTML5 Boilerplate
* Internationalization support
* Sass für CSS design
* NPM
* Webpack
* Testing : Jest & Protractor


<!-- slide -->
<!-- .slide: class="master05" -->
### Server-side Technologien

* Spring Boot
* Spring Security
* Spring MVC REST + Jackson
* Optional Spring Websocket
* Spring Data JPA + Bean Validation
* Maven or Gradle
* Kafka

<!-- slide -->
<!-- .slide: class="master05" -->
### Server-side Technologien - DB

* Liquibase
* Elasticsearch
* NoSQL : MongoDB / Couchbase / Cassandra


<!-- section -->
<!-- .slide: class="master03" -->
### Installation

* JHipster kann ohne Installation via [JHipster Online](https://start.jhipster.tech) verwendet werden (Account erforderlich)
* Installation mit Package-Manager: NPM, Yarn, Homebrew (Mac OS X), Chocolatey (Windows)

```bash
$ yarn global add yo
$ yarn global add generator-jhipster

```
<!-- slide -->
<!-- .slide: class="master03" -->
### Generators
* Yeoman
* Generators
   * Applikation
   * Entity : Command line + JHipster UML & JDL Studio
   * Spring Controller 
   * Spring Service
   * DTO (Beta)

<!-- slide -->
<!-- .slide: class="master03" -->
### Generators
* JHipster Marketplace
* JHipster Modules :  Yeoman generator basiert auf einen JHipster sub-generator

<!-- slide -->
<!-- .slide: class="master03" -->
### Demo Monolithic application

<!-- section -->
<!-- .slide: class="master04" -->
### Microservices mit JHipster

![](../assets/img/jhipster/microservices.png)

<!-- slide -->
<!-- .slide: class="master04" -->
### Microservices - JHipster Registry (1)
* Wird nicht via JHipster generiert - Projekt auf GitHub:
```bash
git@github.com:jhipster/jhipster-registry.git
```
* Eureka Server <small>spring-cloud-netflix</small>
    * Service / Application discovery

<!-- slide -->
<!-- .slide: class="master04" -->
### Microservices - JHipster Registry (2)
* Config Server <small>spring-cloud-config</small>
   * Runtime Configuration für alle Services / Applikationen
<br><br>
* Admin Dashboard zum Monitoren / Managen der Applikationen

<!-- slide -->
<!-- .slide: class="master04" -->
### Microservices - JHipster Gateway
* Wird via JHipster erstellt
* Beinhaltet das UI
* Admin-Interface für Entities / Gateway-Backend
* Proxy / Loadbalancer zu den Microservices
* Accesscontrol / Anbindung OAuth2

<!-- slide -->
<!-- .slide: class="master04" -->
### Microservices - JHipster Console
* Wird nicht via JHipster generiert
* Projekt auf GitHub:
```bash
git@github.com:jhipster/jhipster-console.git
```
* Elasticsearch
* Logstash
* Kibana 

<!-- slide -->
<!-- .slide: class="master04" -->
### Microservices - Demo
* JHipster Registry starten
* Microservice erstellen und Entitiy hinzufügen
* Gateway erstellen und Entity hinzüfgen / importieren 
* Logging aktivieren -> JHipster Console starten
* Hazelcast Management Console aktivieren 

<!-- section -->
<!-- .slide: class="master03" -->
### Pros & Cons
* [+] Best Practises, Guidelines
* [+] Funktionierende Basis -> TTM
* [+] Aktuellster Tech-Stack<br><br>
* [-] Nicht-Standard Applikationen brauchen viel Code-Rückbau
* [-] Dependency-Überraschungen ("Zalando"...)


