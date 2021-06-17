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

GDAL/ogr2ogr is also available
```
> docker-compose run --rm django ogr2ogr --help-general
Creating docker-pg-test_django_run ... done
Generic GDAL utility command options:
  --version: report version of GDAL in use.
  --license: report GDAL license info.
  --formats: report all configured format drivers.
  --format [format]: details of one format.
  --optfile filename: expand an option file into the argument list.
  --config key value: set system configuration option.
  --debug [on/off/value]: set debug level.
  --pause: wait for user input, time to attach debugger
  --locale [locale]: install locale for debugging (i.e. en_US.UTF-8)
  --help-general: report detailed help on general options.
```
