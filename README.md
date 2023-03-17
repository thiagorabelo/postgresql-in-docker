# Postgre in Docker

> :warning:
> Only tested on Ubuntu 22.04

With this configuration you can run PostgreSQL in Docker and
connect to database using `psql` through unix socket as if
PostgreSQL were installed in the machine.

Just install the `postgresql-client` package:

```sh
sudo apt install postgresql-client
```

run the container with `Compose`:

```sh
docker compose up -d
```

and connect to database using `psql`:

```sh
# Maybe you have to create postgres user
# on docker host or create your own $USER
# in the database.
sudo -u postgres -H psql
```
