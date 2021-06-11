# docker-pg-test

A test setup showing how the Azavea postgres and django Docker images can be
connected to each other via docker-compose.

## Usage

In one shell, start the database.
```
$ docker-compose up database
```

In a second shell, run `psql` via the `django` service.
```
docker-compose run --rm django psql
```
