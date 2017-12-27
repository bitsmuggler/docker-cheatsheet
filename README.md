# docker-cheatsheet

## docker

| Beschreibung        | Befehl  |
| ------------- |-------------|
| Alle Docker Container anzeigen| `docker ps -a` |
| Docker Container analysieren|`docker inspect <<Container ID>>`|
| Docker Container stoppen |`docker stop <<Container ID>>`| 
| Docker Container löschen | `docker rm <<Container ID>>`|
| n Docker Container killen|`docker rm -f <<Container Id>> <<Container Id>>`|
|Docker neustarten|`sudo systemctl restart docker`|
|Docker Container verbinden|`docker attach <<Container ID>>`|
|Docker Container Bash ausführen|`docker exec -it <mycontainer> bash`|
|Docker Netzwerke anzeigen|`docker network ls`|
|Docker Netzwerk analysieren (Welche Container laufen in welchem Netzwerk)|`docker network inspect <<netzwerk-name>>`|
|Interne IP von einem Docker Container anzeigen lassen| `docker inspect --format '{{ .NetworkSettings.IPAddress }}' <<Docker Container>>`|
|Nicht mehr benötigte ('dangling') Containers, Volumes und Images löschen.|`docker system prune`|

## docker-compose
docker-compose ermöglicht Docker Container anhand dem docker-compose.yml zu verwalten.

| Beschreibung        | Befehl  |
| ------------- |-------------|
| Docker Container anzeigen| `docker-compose ps` |
| Docker Container bauen|`docker-compose build --no-cache`|
| Docker Container bauen & starten|`docker-compose up -d`| 
| Docker Container stoppen| `docker-compose stop`|
| Docker Container löschen|`docker-compose rm -f`|
| Docker Container stoppen und löschen|`docker-compose down`|
| Docker Container Logs anzeigen|`docker-compose logs`|
| Logs von einem bestimmten Service anzeigen|`docker-compose logs -f <<myservice>>`|
| Docker Services anzeigen|`docker-compose config --services`|
