# Docker Compose

- - - -

## Table of Contents

* [What is Docker compose?](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/dockerCompose.md#what-is-docker-compose)
* [Example](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/dockerCompose.md#example)

## What is docker-compose?

* Often you typically have several applications running in conjunctions (especially when using microservices) e.g. a web application with a FE, cache and database
* `docker-compose` files allows you to define multiple service in a 'stack' and run them at once
* `docker-compose` are written in a declarative style (YML)
* These are called "multi container" apps

### Command

`docker-compose up -d` Uses a docker compose file to start multiple containers in detached mode

## Example

Example `docker-compose` file

```docker
version: "3.9"
services:
  web:
    build: .
    ports:
      - "5000:5000"
  redis:
    image: "redis:alpine"

```