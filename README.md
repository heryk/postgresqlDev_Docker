# Postgesql _Docker

## Commandes Docker pour se créer un environnment Postgresql de test/développement

Allez chercher l'image:

`docker pull postgres`

Créer un dossier local (mount) pour sauvegarder les données postgresql. ¨ca permet de ne pas perdre les données si vous supprimer le container Docker: 

`mkdir -p C:\Users\hjulien\DockerMounts\pg`

Faire rouler Docker avec le mount créé précédemment:

`docker run --rm   --name pg-docker -e POSTGRES_PASSWORD=postgres -d -p 5432:5432 -v C:\Users\hjulien\DockerMounts\pg:/var/lib/postgresql/data  postgres`


## Info de connection avec PGAdmin ou DBeaver:
- Host: localhost
- Port: 5423
- DB: postgres
- User: postgres

## Allez chercher la liste complète des conainers qui roulent. Affiche également l'identifiant unique de l'instance de postgrsql qui roule:
`docker ps`

## Supprimer un container spécifique. Remplacez [container id] par l'id de postgresql qui roule:
`docker kill [container id]`


## Autres infos utiles:
- PostgreSQL Docker Image: https://hub.docker.com/_/postgres
- PostgreSQL in Docker & Docker Volume Mounting: https://faun.pub/postgresql-in-docker-mount-volume-3220fbd0afc4