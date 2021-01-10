FROM postgres:12.5

ENV HOME=/var/lib/pgsql \
    POSTGRES_USER=postgres \
    POSTGRES_PASSWORD=postgres \
    PG_USER_DIR=/opt/postgres/inventory \
    PG_INIT_DB=/docker-entrypoint-initdb.d

USER root

RUN mkdir -p $PG_USER_DIR

COPY createDB.sql $PG_INIT_DB

RUN chmod 777 $PG_INIT_DB/createDB.sql

EXPOSE 5432
