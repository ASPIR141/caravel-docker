# Caravel
A Docker image for Airbnb's Caravel data visualization platform.

## Setup
Run the docker container by entering this commands into your console:

```bash
  docker build --tag <your username>/caravel .
  docker run --name caravel --publish 8088:8088 --detach <your username>/caravel
```
After starting of the container, navigate to [http://localhost:8088/](http://localhost:8088/) to get started with Caravel.

## Documentation
The official documentation is available here:
[http://airbnb.io/caravel/](http://airbnb.io/caravel/)

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
