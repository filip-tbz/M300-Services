# Wordpress Setup

Ich habe als Zusatz ein Wordpress Container erstellt mit MySQL und PHPmyAdmin. Da es hier um mehrere Services handelt, habe ich diese mit Docker Compose zusammengestellt.

Zuerst muss man Docker Compose installieren, falls dies noch nicht installiert wurde:

                    root@docker_m300:/home/tbzsaii# apt install docker-compose

Danach habe ich auf Visual Studio Code mein .YAML Datei erstellt und bearbeitet. Auf dieser Seite finden sie, was ich installiert habe dafür. Die Datei finden sie hier: 

[Docker-Compose-File](https://github.com/tbzsaii/M300-Services/blob/master/30-Container/00-Wordpress/docker-compose.yaml)

Ich habe die Datei in einem Verzeichnis abglegt, welches ich selber erstellt habe. Die Datei finden sie unter */lib/docker/wp/*.

Wenn die .YAML stimme sollte und es keine Fehler in der Datei gibt, kann man mit dem folgenden Befehl die Container installieren:

                    root@docker_m300:/lib/docker/wp# docker-compose up -d

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/docker%20compose.png "docker compose")

Damit wir sicher sind, dass die Container installiert wurden, kann man diesen Befehl `docker ps` ausführen. So sollte es dann aussehen:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/docker%20ps%20wp.png "wordpress docker ps")

Danach sollte auch schon Wordpress funktionieren. Geben sie einfach http://localhost:8000/ in den Browser ein und dann sollte ein Installationsfenster auftauchen, welches wie im folgenden Bild aussieht:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/test%20wp.png "docker wp install")

Hat man sich erfolgreich installiert, kann man sich einloggen mit den definiertem User und Passwort und sollte dann auch das Dashboard von Wordpress angezeigen:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/login%20wp.png "Login WP")

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/dashboard%20wp.png "WP Dashboard")

## phpMyAdmin

Um phpMyAdmin zu testen, gibt http://localhost:8080/ in den Browser ein, dann sollte auch das Anmeldefesnter von phpMyAdmin auftauchen:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/phpmyadmin.PNG "phpMyAdmin-Login")


