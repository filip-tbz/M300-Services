# Dokumentation Lernbeurteilung 2
![alt text](https://www.itprotoday.com/sites/itprotoday.com/files/styles/article_featured_retina/public/Cloud%20with%20light%20coming%20from%20it%20and%20connected%20vectors%20within.jpg?itok=9i48eejV "Cloud")

**Modul 300, FR20, Lehrer: Philip Rohr, Autor: Shagithijan Baasgaran** 

## Kriterien 1

          VirtualBox
          Vagrant
          Visualstudio-Code
          Git-Client
          SSH-Key für Client erstellt

### VirtualBox 
![alt text](https://raw.githubusercontent.com/tbzsaii/M300-Services/master/img/virtualbox_version.PNG "Virtualbox Version")

### Vagrant
Folgend sehen sie die Version der installierten Vagrant-Applikation:

          AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~
          $ vagrant -v
          vagrant 2.2.7

### Visual Studio Code
Nach der Installation wurden 3 weitere wichtige Extensions hinzugefügt:

  Markdown All in One
  
            Name: Markdown All in One
            Id: yzhang.markdown-all-in-one
            Description: All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
            Version: 2.7.0
            Publisher: Yu Zhang

  Vagrantfile Support
  
            Name: Vagrantfile Support
            Id: marcostazi.vs-code-vagrantfile
            Description: Provides syntax highlighting support for Vagrantfile, useful if you use Vagrant
            Version: 0.0.7
            Publisher: Marco Stazi

  vscode-pdf Extension

            Name: vscode-pdf
            Id: tomoki1207.pdf
            Description: Display pdf file in VSCode.
            Version: 0.5.1
            Publisher: tomoki1207


   ![alt text](https://github.com/tbzsaii/M300-Services/blob/master/img/visualstudiocode_version.PNG "Visual Studio Code Version")

### Git-Client
Folgend sehen sie die Version des installierten Git-Clients:

          AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~
          $ git --version
          git version 2.25.0.windows.1

### SSH-Key für Client erstellt

          ssh -v git@github.com
          [...]
          debug1: Authentications that can continue: publickey
          debug1: Next authentication method: publickey
          debug1: Offering public key: /c/Users/ShagithijanBaasgaran/.ssh/id_rsa RSA SHA256:KN
          [...]

## Kriterien 2

          Github-Account ist erstellt
          Git-Client wurde verwendet
          Dokumuentation ist als Mark Down vorhanden
          Mark Down-Editor ausgewählt und eingerichtet
          Mark Down ist stukturiert
          Persönlicher Wissenstand
          Wichtige Lernschritte

### Github-Account

[Github-Account von Shagithijan Baasgaran](https://github.com/tbzsaii)

### Git-Client

Hier ein Beweis, dass der Git-Client verwendet wurde:

### Mark Down Dokumentation

Ich habe die Dokumentation in der README.md Datei erfasst. Das diese in Mark Down geschrieben wurde sollte ersichtlich sein.

### Mark Down Editor

Ich habe in diesem Fall kein Mark Down Editor benutzt, sondern die README.md Datei in Visual Studio Code bearbeitet, gespeichert, commited und gepusht. Als Alternative hatte ich noch den Editor Atom zur Verfügung, jedoch verwendete ich diesen nicht für die Dokumentation.

### Mark Down ist strukturiert

Die Dokumentation habe ich so aufgebaut, dass bereits alle Kriterien der Lernbeurteilung ersichtlich sind und ob diese erfüllt wurden oder nicht. 

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

## Kriterien 3

            Bestehende VM aus Vagrant-Cloud einrichten
            Vagrant-Befehle
            Umgebung dokumentiert
            Funktionsweise getestet inkl. Testfälle
            andere vorgefertigte VM auf eigenem Notebook
            Projekt mit Git und Mark Down dokumentiert

### Bestehende VM aus Vagrant-Cloud

### Vagrant-Befehle

| Befehl              | Funktion       |
| ------------------- | -------------- |
| `vagrant init`      | Dadurch wird das aktuelle Verzeichnis als Vagrant-Umgebung initialisiert, indem eine erste Vagrant-Datei erstellt wird, falls eine solche noch nicht vorhanden ist.|
| `vagrant up`        | Dieser Befehl erstellt und konfiguriert Gast-Rechner entsprechend Ihrer Vagrantdatei.|
| `vagrant ssh`       ||
| `vagrant status`    ||
| `vagrant provision` ||
| `vagrant halt`      ||
| `vagrant destroy`   ||

### Eingerichtete Umgebung ist dokumentiert

### Testfälle

### vorgefertigte VM eingerichtet

### Projekt mit Git und Mark Down dokumentiert

## Kriterien 4

            Firewall eingerichtet
            Reverse-Proxy eingerichtet
            Benutzer- und Rechtevergabe
            Zugang mit SSH-Tunnel abgesichert
            Sicherheitsmassnahmen dokumentiert
            Projekt mit Git und Mark Down dokumentiert

### Firewall

Mit folgendem Beispiel kann der Status der Firewall und die eingetragenen Regeln aufgerufen werden:

            $ ufw status

### Reverse-Proxy

### Benutzer- und Rechtevergabe

### Zugang mit SSH-Tunnel

### Sicherheitsmassnahmen

### Projekt mit Git und Mark Down dokumentiert

## Kriterien 5

                Standard Befehle
                Reflexion
                Wissenserweiterung / Fortschritt
                Links

### Standard Befehle
Visual Studio Code öffnen:

`code`
 
Verzeichnis wechseln:

`cd [PATH]`

CLI schliessen:

`exit`

## Reflexion

## Links

[Markdown Cheat-Sheet](https://www.markdownguide.org/cheat-sheet/)
[Vagrant Befehle](https://www.vagrantup.com/docs/)