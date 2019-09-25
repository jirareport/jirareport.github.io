---
layout: default
title: Como instalar
permalink: /install
nav_order: 2
---

# Instalação utilizando docker

A instalação do jiratório pode ser feita através das imagens que estão no próprio [docker hub](https://hub.docker.com/u/jirareport).

Exemplo de docker-compose.yml:


```yml
version: "3.4"

services:
  jirareport-api:
    image: jirareport/jirareport-api:latest
    restart: always
    environment:
      SPRING_DATASOURCE_URL: "jdbc:postgresql://<database-host>:5432/<database-name>"
      SPRING_DATASOURCE_USERNAME: "<username>"
      SPRING_DATASOURCE_PASSWORD: "<password>"
      HOLIDAY_TOKEN: "<token>"
      SECURITY_KEY: "<key>"
      JIRA_URL: "<jira-url>"
  jirareport-web:
    image: jirareport/jirareport-web:latest
    restart: always
    environment:
      JIRAREPORT_API_URL: "http://jirareport-api"
    ports:
      - 80:80
    depends_on:
      - jirareport-api
```

Substítua:

|Placeholder|Valor|Exemplo|
|---|---|---|
|\<username\>|Nome do usuário do banco de dados postgres|leferreira|
|\<password\>|Senha do usuário do banco de dados postgres|123123|
|\<token\>|Token de feriados padrão gerado em http://www.calendario.com.br/api_feriados_municipais_estaduais_nacionais.php|mY4lWZvxkZ3BWau52diVmLl5dZCoYXNoPTY0NzIzNDcy|
|\<key\>|Chave utilizada para criptografar o token JWT|super-secret-token|
|\<database-host\>|IP do host em que o banco de dados postgres está instalado|192.168.6.66|
|\<database-name\>|Schema do banco de dados postgres|jirareport|
|\<jira-url\>|URL do jira que o jiratório coletará métricas|https://jirareport.atlassian.net|

## Exemplo completo de docker compose com aplicações e banco de dados

```yml
version: "3.4"

services:
  jirareport-database:
    image: postgres:9.6
    restart: always
    environment:
      POSTGRES_USER: jirareport
      POSTGRES_PASSWORD: troperarij
      POSTGRES_DB: jirareport
    volumes:
      - "./data/postgres:/var/lib/postgresql/data"
  jirareport-api:
    image: jirareport/jirareport-api:latest
    restart: always
    environment:
      SPRING_DATASOURCE_URL: "jdbc:postgresql://jirareport-database:5432/jirareport"
      SPRING_DATASOURCE_USERNAME: "jirareport"
      SPRING_DATASOURCE_PASSWORD: "troperarij"
      HOLIDAY_TOKEN: "<token>"
      SECURITY_KEY: "<key>"
      JIRA_URL: "<jira-url>"
    depends_on:
      - jirareport-database
  jirareport-web:
    image: jirareport/jirareport-web:latest
    restart: always
    environment:
      JIRAREPORT_API_URL: "http://jirareport-api"
    ports:
      - 80:80
    depends_on:
      - jirareport-api
```
