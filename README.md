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


### Persönlicher Wissenstand

| Thema                  | Wissenstand                                                          |
| ---------------------- | -------------------------------------------------------------------- |
| Linux                  | Linux habe ich bereits im ÜK gelernt und mehrmals in den Modulen. Linux ist ein vertrautes Betriebssystem mit dem ich ohne Probleme umgehen kann.|
| Virtualisierung        | Mit Virtualisierung habe ich bereits gearbeitet, jedoch nicht mit Virtual Box. im Normalfall habe ich immer vmWare Workstation benutzt. |
| Vagrant                | Der Begriff Vagrant kam mir das erste Mal in diesem Modul zu Ohren. Ich habe diese Methode nie gekannt.|
| Versionsverwaltung/Git | Mit Git habe ich erst kürzlich in der Abteilung verwendet, jedoch nicht so, wie ich es jetzt in diesem Modul benutze. Ich wusste aber, dass es diese Methode gibt.|
| Mark Down              | Alle meine Dokumentation wurden normal im Word aufgesetzt. Zum ersten Mal verwende ich Mark Down und bin sehr begeistert davon.|
| Systemsicherheit       | Systemsicherheit war immer ein Thema in jedem Modul. Ich bin mir von den Möglichkeiten bewusst und weiss wie sie am beste anzuwenden sind.|

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
Zuerst müssen wir ins Verzeichnis wechseln und danach die VM starten:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~
            $ cd Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web/

Danach muss die VM vie `vagrant up` gestartet werden:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~/Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web (master)
            $ vagrant up 



### Vagrant-Befehle

| Befehl              | Funktion       |
| ------------------- | -------------- |
| `vagrant init`      | Dadurch wird das aktuelle Verzeichnis als Vagrant-Umgebung initialisiert|
| `vagrant up`        | Dieser Befehl startet den Gast-Rechner/Virtuelle Maschine.|
| `vagrant ssh`       | Dadurch wird SSH in einen laufenden Vagrant-Rechner eingespielt und man erhält Zugriff auf die Shell.|
| `vagrant status`    | Dadruch wird der aktuelle Status des Gastrechners angezeigt. |
| `vagrant provision` | Dadruch wird der Gast-Rechner aktualisiert, nachdem Änderungen an der Vagrant-Datei vorgenommen wurden.|
| `vagrant halt`      | Dadurch wird der Gast-Rechner heruntergefahren. |
| `vagrant destroy`   | Dadurch werden alle Ressourcen, die erstellt wurden zum Gast-Rechner und der Gast-Rechner selbst gelöscht.|

Für weitere Befehle, gehen sie auf diese Website: [Vagrant Befehle](https://www.vagrantup.com/docs/cli/)

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