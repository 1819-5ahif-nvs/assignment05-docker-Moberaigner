# 1819_5ahif_nvs_assignment05_docker

## Starten
Docker Compose file builden (um alle Container zu Konfigurieren):
docker-compose up --build

Thorntail Projekt builden und ausführen:
mvn package

cd target
java -jar demo-thorntail.jar

## Docker
Folgende Services werden in Docker Containern aufgesetzt:

- nginx webserver (Port 80)
- wildfly Application Server (Port 8080)
- mysql (Port 3306)
- phpmyadmin (Port 5050)

## Cheatsheet

- FROM
beinhaltet ein fertiges Image. Man kann als Basis z.B. ein Betriebssystem verwenden (FROM ubuntu:latest)

- RUN
Man kann Linux-Befehle für die Shell ausführen. z.B "RUN mkdir /www && touch index.html"

-COPY
Dateien können in den Container geladen oder überschrieben werden.

- ADD
Dateien können in den Container geladen oder überschreiben werden => auch mit URL möglich z.B ADD http://example.com/big.tar.xz /usr/src/things/


- EXPOSE
Ein Container kann ein bestimmter Port zugewiesen werden. z.B EXPOSE 80
