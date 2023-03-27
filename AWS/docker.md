# Docker 
`Docker build -t simple-node .` will create a docker image named simple node
`docker images` will print all the available images.
a docker image is used to create a docker container.

`docker build .` exécutera le Dockerfile pour créer une image
`docker images` imprimera toutes les images disponibles
`docker run {IMAGE_ID}` lancera un conteneur avec l'image
`docker ps` affichera tous les conteneurs en cours d'exécution.
`docker kill {CONTAINER_ID}` terminera le conteneur

`docker logs [OPTIONS] CONTAINER` for logs
`docker exec -it my_container sh` to open shell in a container
`docker ps [OPTIONS]` to see running container IDs.
`docker inspect [OPTIONS] NAME|ID [NAME|ID...]` Return low-level information on Docker objects


Création et utilisation d'un dépôt DockerHub
Dans DockerHub, créez un nouveau dépôt et définissez-le sur Public.

Dans votre terminal, connectez-vous à DockerHub

`docker login --username={YOUR USERNAME}`
Marquez votre image locale avec le nom du dépôt :
`docker tag {{LOCAL IMAGE NAME} {USERNAME}/{REPOSITORY NAME}`
Poussez l'image vers DockerHub
`docker push {TAGGED IMAGE}`