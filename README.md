# Commandes Docker pour se créer un environnment Postgresql de test/développement

 docker pull postgres

 mkdir -p C:\Users\hjulien\DockerMounts\pg

 docker run --rm   --name pg-docker -e POSTGRES_PASSWORD=postgres -d -p 5432:5432 -v C:\Users\hjulien\DockerMounts\pg:/var/lib/postgresql/data  postgres


# Info de connection avec PGAdmin ou DBeaver:

Host: localhost
Port: 5423
DB: postgres
User: postgres

# List all / Show Active container
 docker ps

# Kill a specific container
 docker kill [container id]


# Infos utiles:
- PostgreSQL Docker Image: https://hub.docker.com/_/postgres
- PostgreSQL in Docker & Docker Volume Mounting: https://faun.pub/postgresql-in-docker-mount-volume-3220fbd0afc4