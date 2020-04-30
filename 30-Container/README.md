# 30 Container

## Netzwerkumgebung

So stelle ich mir die Umgebung am Schluss vor:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/netzwerkplan%20docker.PNG "Docker Netzwerkplan")


## Docker Installation
Ich habe Docker auf einer Linux-Umgebung installiert. Dafür habe ich Virutalbox gewählt, da ich bereits meine Kenntnisse gesammelt habe in der vorherigen Übung. 

Um Docker zu installieren, können sie die folgende Anleitung befolgen [Docker Installation](https://docs.docker.com/engine/install/ubuntu/)

*Kleiner Tipp: Arbeitet im Superuser-Modus.*

Nach der Installation, kann man testen, ob Docker funktioniert. Daür brauchen wir folgenden Befehl:

`root@docker_m300:/home/tbzsaii# docker run hello-world `

Danach sollte es so aussehen:
![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/docker_run.PNG "Docker Run")

Damit ich keine Probleme mit den Rechten und dem Pushen in das Dockerhub bekomme, habe ich mich zuerst noch eingeloggt mit dem folgenden Befehl:

`root@docker_m300:/home/tbzsaii# docker login`

## Backend und Frontend Container
Ich habe für diese Lernbeurteilung zwei Container erstellt. Ich habe dafür einen Apache Server als Backend eingerichtet und MySQL als Frontend.

Apache Backend: `docker container run -d -p 8081:80 --name MyApache httpd`

MySQL Frontend: `docker container run -it -p 8082:80 mysql`

 ![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/docker%20ps%20a.PNG "docker ps -a")

 Wenn die Container installiert sind, kann man den Webserver auf dem Browser aufrufen. Dafür einfach http://localhost:8081 eingeben. So sieht es aus, wenn es funktioniert hat:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/test%20apache.PNG "apache test")


## Volumes zu persisten Datenablage eingerichtet

## Docker Befehle
| Befehl              | Funktion       |
| ------------------- | -------------- |
| `docker ps -a`      | Dadurch werden Container aufgelistet.|
| `docker container ls -a`        | Dadurch werden Container aufgelistet, auch die offline.|
| `docker container stop [ID]`       | Dadurch wird ein Container beendet.|
| `docker ps -aq`    | Dadurch werden alle Container gestoppt.|
| `docker container exec -it [NAME] bash` | Dadurch wird ein Container ausgeführt und betreten.|
| `docker images` | Dadurch werden die Images angezeigt.|
| `docker image build -t` | Dadurch kann man ein Image erstellen.|

## Testfälle

| Testfall                      | OK/Nicht OK    |
| --------                      | -------------- |
| Container können angezeigt werden.      | positiv        |
| Webserver ist erreichbar           | positiv        |
| Applikation ist erreichbar        | positiv        |
| Ports sind nicht besetzt, überschneiden sich nicht     | positiv        |
| Image wurde erstellt            | positiv        |
| Dockerhub ist erreichbar    | positiv        |


# Image Bereitstellung
