# Docker File to run the Rates Postgres database
####STAGE 1: BUILD#####
FROM postgres:13.5
ENV POSTGRES_USER postgres
ENV POSTGRES_PASSWORD pass123

####STAGE 2: RUN#####
COPY rates.sql /docker-entrypoint-initdb.d/