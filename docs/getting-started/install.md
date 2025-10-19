---
title: Getting started with Ranger
---
[Docker Docs]: https://docs.docker.com/get-started/overview/
# Installation
!!! tip
    If you don't have prior experience with Docker 🐳, we recommend reading
    [Docker Docs], which provides extensive documentation around how to get started with Docker.
### docker <small>recommended</small> { #docker data-toc-label="docker" }

The official [Docker image] is a great way to get up and running in a few
minutes, as it comes with all dependencies pre-installed. Open up a terminal
and pull the image using:

=== "Latest"

    ```
    docker pull apache/ranger
    docker pull apache/ranger-db
    docker pull apache/ranger-solr
    docker pull apache/ranger-zk
    ```

=== "2.7"

    ```
    docker pull apache/ranger:2.7.0
    docker pull apache/ranger-db:2.7.0
    docker pull apache/ranger-solr:2.7.0
    docker pull apache/ranger-zk:2.7.0
    ```

???+ warning

    The Docker container is intended for development purposes only and
    is not suitable for production based deployment.
    [Docker Image]: https://hub.docker.com/r/apache/ranger


### docker compose <small> for services </small> { #docker-compose data-toc-label="docker-compose" }
To bring up different data processing services (with Ranger plugin installed), `docker compose` is recommended.

Follow instructions here to get started: [Ranger Services with Docker Compose](https://github.com/apache/ranger/blob/master/dev-support/ranger-docker/README.md)

