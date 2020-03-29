# Git Repository M300-Services
**Modul 300, FR20, Lehrer: Philip Rohr, Autor: Shagithijan Baasgaran** 

In diesem Repository finden sie alle Dateien zur Lernbeurteilung 2

## QuickLinks

[title](https://www.example.com)
[title](https://www.example.com)
[title](https://www.example.com)
[title](https://www.example.com)
[title](https://www.example.com)
[title](https://www.example.com)
[title](https://www.example.com)


### Wichtige Lernschritte

| Thema                 | Lernschritte |
|-----------------------|--------------|
|Vagrant                | Von diesem Programm konnte ich in diesem Fach sehr profitieren. Vieles wusste ich garnicht und bin auch froh, dass ich dies lernen durfte, da ich in der nächsten Abteilung Vagrant anwenden kann.|
|Mark Down              | Mark Down ist eine interessante Sprache, die man in der Freizeit lern|

## Kriterien 3

            Bestehende VM aus Vagrant-Cloud einrichten
            Vagrant-Befehle
            Umgebung dokumentiert
            Funktionsweise getestet inkl. Testfälle
            andere vorgefertigte VM auf eigenem Notebook
            Projekt mit Git und Mark Down dokumentiert

### Bestehende VM aus Vagrant-Cloud


### Vagrant-Befehle


### Eingerichtete Umgebung ist dokumentiert

Netzwerkplan:

![alt text](https://raw.githubusercontent.com/tbzsaii/M300-Services/master/img/netzwerkplan.PNG "Netzwerkplan")

In meiner Umgebung wurde folgendes erstellt, installiert und konfiguriert:
 - Apache Webserver
 - UFW wurde konfiguriert
 - SSH Zugang
 - Reverse Proxy

### Testfälle

### vorgefertigte VM eingerichtet

## Kriterien 4

            Firewall eingerichtet
            Reverse-Proxy eingerichtet
            Benutzer- und Rechtevergabe
            Zugang mit SSH-Tunnel abgesichert
            Sicherheitsmassnahmen dokumentiert
            Projekt mit Git und Mark Down dokumentiert

### Firewall

Mit folgendem Beispiel kann der Status der Firewall und die eingetragenen Regeln aufgerufen werden:

            shagithijan@lxwsrv01:~$ sudo ufw status
            Status: active

            To                         Action      From
            --                         ------      ----
            22                         ALLOW       Anywhere
            8080                       ALLOW       Anywhere
            22 (v6)                    ALLOW       Anywhere (v6)
            8080 (v6)                  ALLOW       Anywhere (v6)

            Anywhere                   DENY OUT    Anywhere
            Anywhere (v6)              DENY OUT    Anywhere (v6)

            shagithijan@lxwsrv01:~$


### Reverse-Proxy

Der Reverse-Proxy wurde auch mit installiert und anhand der Anleitung aufgesetzt. 

            root@lxwsrv01:/etc/apache2/sites-available# cat 001-reverseproxy.conf
            # Allgemeine Proxy Einstellungen
            ProxyRequests Off
            <Proxy *>
                    Order deny,allow
                    Allow from all
            </Proxy>

            # Weiterleitungen master
            ProxyPass /master http://master
            ProxyPassReverse /master http://master



### Benutzer- und Rechtevergabe

Es wurden keine Benutzer und keine besonderen Rechte zugewiesen. Ich habe alles so belassen, wie es auch aufgesetzt wurde. Der SSH-Benutzer wurde standardmässig erstellt. 

Erstelle Benutzer sind in der folgenden Datei ersichtlich:

            /etc/passwd

### Zugang mit SSH-Tunnel

Der Zugang über SSH zum Webserver erfolgt leider nicht wie geplant. Ich kann über den Git-Client auf den Server mit `vagrant ssh` verbinden. Benutzer wurde standardmässig erstellt:

            username: vagrant

### Sicherheitsmassnahmen

In diesem Dokument wurden folgende Sicherheitsmassnahmen dokumentiert:

            - [x] Firewall mit Regeln
            - [ ] SSH Zugang
            - [x] Reverse Proxy 


## Kriterien 5

                Standard Befehle
                Reflexion
                Wissenserweiterung / Fortschritt
                Links

### Nützliche Befehle

| Befehl                  | Funktion       |
| ----------------------- | -------------- |
| `eval 'ssh-agent'`      | Hintergrundprogramm, das Passwörter für private SSH-Schlüssel behandelt, aufrufen.|
| `ssh-add`               | Fordert den Benutzer zur Eingabe eines Passworts für den privaten Schlüssel auf und fügt es der Liste hinzu, die vom SSH-Agenten verwaltet wird. |
| `sudo su`               | Root Benutzer auswählen.|
| `code`                  | Visual Studio Code öffnen.|
| `cd [PATH]`             | Verzeichnis wechseln.|
| `exit`                  | CLI schliessen.|


### Reflexion 

Im gesamten hat mir diese Lernebeurteilung gefallen. Jedoch hat sie mir öfters Schwierigkeiten bereitet. Zu Beginn wusste ich kein einziges Fachbegriff zu diesem Thema und zurzeit könnte ich bei vielen Gesprächen, welche um dieses Thema handeln, mitreden. Es freut mich zu sehen, dass ich Fortschritt gemacht habe und viel Wissen mitnehmen konnte. 

### Links

[Markdown Cheat-Sheet](https://www.markdownguide.org/cheat-sheet/)

[Vagrant](https://www.vagrantup.com/docs/)