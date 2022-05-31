### Starting Docker Compose

Checkout the repository or download the sources.

Simply run `docker-compose up -d` and you are done.

PostgreSQL will be available on `localhost:5432`;
Kafka will be available on `localhost:9092`;
Zookeper will be available on `localhost:2181`;
Keycloak will be available on `localhost:28080`;
Flagr will be available on `localhost:18000`;
Redis will be available on `localhost:6379`;
Mongo will be available on `localhost:27017`;

### Using PostgreSQL

Default connection:

`docker-compose exec db psql -U postgres`

Using .env file default parameters:

`docker-compose exec db psql -U dbuser dbname`

## Clear cache

```
docker-compose rm --all
docker-compose pull
docker-compose build --no-cache
docker-compose up -d --force-recreate
 ```