# Caravel
A Docker image for Airbnb's Caravel data visualization platform.

[![](https://img.shields.io/docker/pulls/aspir/caravel-docker.svg)](https://hub.docker.com/r/aspir/caravel-docker "Click to view the image on Docker Hub")
[!(https://img.shields.io/docker/automated/aspir/caravel-docker.svg)]
[![Documentation](https://img.shields.io/badge/docs-airbnb.io-blue.svg)](http://airbnb.io/caravel/)

## Setup
Run the docker container by entering this commands into your console:

```bash
  docker build --tag <your username>/caravel .
  docker run --name caravel --publish 8088:8088 --detach <your username>/caravel
```
After starting of the container, navigate to [http://localhost:8088/](http://localhost:8088/) to get started with Caravel.

## Documentation
The official documentation is available here:
[http://airbnb.io/caravel/](http://airbnb.io/caravel/).

## Database setup

### PostgreSQL
```bash
  docker run --name caravel --publish 8088:8088 --detach \
          --env SECRET_KEY="mySUPERsecretKEY" \
          --env SQLALCHEMY_DATABASE_URI="postgresql://user:pass@host:port/db" \
          <your username>/caravel
```
### MySQL
```bash
  docker run --name caravel --publish 8088:8088 --detach \
          --env SECRET_KEY="mySUPERsecretKEY" \
          --env SQLALCHEMY_DATABASE_URI="mysql://user:pass@host:port/db" \
          <your username>/caravel
```
