# 35-Sicherheit

## Speicher Begrenzung
Durch die Begrenzung des verfügbaren Speichers schützen man sich vor DoSAngriffen und Anwendungen mit Speicherlecks, die nach und nach den Speicher auf dem Host auffressen.

`docker run -m 128m --memory-swap 128m amouat/stress stress --vm 1 --vm-bytes 127m -t 5s`

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/speicher%20docker.PNG "Speicher Begrenzung")


## Neustart Begrenzung
Stirbt ein Container immer wieder und wird dann neu gestartet, muss das System nicht unerheblich Zeit und Ressourcen aufwenden, was im Extremfall auch zu einem DoS führen kann.

`docker run -d --restart=on-failure:10 httpd`

`docker run -d --restart=on-failure:10 mysql`

Ich habe für beide Container dieses Sicherheitsaspekt ausgeführt. Folgend sehen sie einen Beweis:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/mysql%20neustart.PNG "neustart mysql")

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/httpd%20neustart.PNG "neustart httpd")

## Ressourcenbeschränkung

Der Linux-Kernel definiert Ressourcenbeschränkungen, die für Prozesse gesetzt werden können – z.B. die Anzahl der Kind-Prozesse, die sich forken lassen, oder die Anzahl der zulässigen offenen File-Deskriptoren.

Diese lassen sich auch auf Docker-Container anwenden – durch Übergabe des Flags `--ulimit` an `docker run`.

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/ressourcenbeschr%C3%A4nken.PNG "ressourcenbeschränkung")

## Cadvisor
Ich habe zusätzlich ein Überwachungstool installiert. Nämlich cAdvisor, welches von Google erstellt wurde und das meist benutzte Monitoring-Tool ist.

Dazu habe ich den folgenden Befehl ausgeführt:

`docker run -d --name cadvisor -v /:/rootfs:ro -v /var/run:/var/run:rw -v /sys:/sys:ro -v /var/lib/docker/:/var/lib/docker:ro -p 8080:8080 google/cadvisor:latest`

Wenn das geklappt hat, kann man den Browser öffnen und http://localhost:8080 öffnen. So wird es dann aussehen:

![](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/cadvisor.PNG "cadvisor")


