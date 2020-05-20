# docker-compose.yml

Docker Compose is an official tool supplied by Docker. At its core, it’s a utility that lets you “compose” Docker commands and manage multiple containers in an easy way.

# Structuur van de file
De docker-compose.yml file moet volgens een bepaalde layout aangemaakt worden.

[https://docs.docker.com/compose/compose-file/](https://docs.docker.com/compose/compose-file/)

## version
Er zijn verschillende versies van layouts met zijn eigen specificaties.
de versie is een verplicht onderdeel van de file

## services
Onder dit verplichte key kan je een of meer configuraties maken voor containers

voorbeeld

```
version: "3.8"
services:
  webapp:
  
  database:
  
```
elke container configuratie heeft zijn eigen settings