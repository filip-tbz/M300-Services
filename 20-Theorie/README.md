# 25-Benutzer und Rechte

## Inhalt
  - [Benutzer und Rechte](#benutzer-und-rechte)
  - [Container](#container)
  - [Docker](#docker)

## Benutzer und Rechte
Wie bei allen Betriebssysteme gibt es auch im Linux Benutzer und Rechte. Nebst den Benutzer die wir erstellen, gibt es noch verschiedene Systemdienste, die über eigene Konten verfügen:

| Benutzername  | Funktion                                             |
| ------------- | ---------------------------------------------------- | 
| `root`        | Der Systemadministrator unter Linux                  |
| `nobody`      | Wird von Prozessen als Benutzererkennung verwendet, wenn nur ein Minimum an Rechten vergeben werden soll  |
| `cupsys`      | Benutzer des Druckdienstes CUPS                      |
| `www-data`    | Benutzer des Webservers Apache                       |

Die Benutzer werden in einer zentralen Datei gespeichert. Die Benutzer findet man in `/etc/passwd` und die Passwörter zu den Benutzer in `/etc/shadow`.

Wie in allen Systemen, gibt es einen Systemadministrator, hier "root", welcher über alle Rechte verfügt. 

Berechtigungen werden über ein Konzept verteilt. Die Berechtigungen werden mit Zahlen versehen.

| Berechtigung | Wert |
| ------------ | ---- |
|     ---      | 0    |
|     --x      | 1    |
|     -w-      | 2    |
|     -wx      | 3    |
|     r--      | 4    |
|     r-x      | 5    |
|     rw-      | 6    |
|     rwx      | 7    |

Folgende Befehle können zum Ändern der Rechte nützlich sein:

| Befehl        | Funktion                                             |
| ------------- | ---------------------------------------------------- | 
| `chmod`       | Dient zum Setzen der Dateirechte                     |
| `chown`       | Dient zum Ändern des Dateibesitzers                  |
| `chgrp`       | Dient zum Ändern der Gruppe einer Datei              |

## Container
Container ändern die Art und Weise, wie wir Software entwickeln, verteilen und laufen lassen, grundlegend.

Entwickler können Software lokal bauen, die woanders genauso laufen wird – sei es ein Rack in der IT-Abteilung, der Laptop eines Anwenders oder ein Cluster in der Cloud.

Administratoren können sich auf die Netzwerke, Ressourcen und die Uptime konzentrieren und müssen weniger Zeit mit dem Konfigurieren von Umgebungen und dem Kampf mit Systemabhängigkeiten verbringen.

**Merkmale** <br>
* Container teilen sich Ressourcen mit dem Host-Betriebssystem
* Container können im Bruchteil einer Sekunde gestartet und gestoppt werden
* Anwendungen, die in Containern laufen, verursachen wenig bis gar keinen Overhead
* Container sind portierbar --> Fertig mit "Aber bei mir auf dem Rechner lief es doch!"
* Container sind leichtgewichtig, d.h. es können dutzende parallel betrieben werden.
* Container sind "Cloud-ready"!

## Docker
Docker nahm die bestehende Linux-Containertechnologie auf und verpackte und erweiterte sie in vielerlei Hinsicht – vor allem durch portable Images und eine benutzerfreundliche Schnittstelle –, um eine vollständige Lösung für das Erstellen und Verteilen von Containern zu schaffen.

Die Docker-Plattform besteht vereinfacht gesagt aus zwei getrennten Komponenten: der Docker Engine, die für das Erstellen und Ausführen von Containern verantwortlich ist, sowie dem Docker Hub, einem Cloud Service, um Container-Images zu verteilen.

**Wichtig:** Docker wurde für 64-bit Linux Systeme entwickelt, kann jedoch auch mittels VirtualBox auf Mac und Windows betrieben werden.


### Architektur
***

Nachfolgend sind die wichtigsten Komponenten von Docker aufgelistet:

**Docker Deamon** <br>
* Erstellen, Ausführen und Überwachen der Container
* Bauen und Speichern von Images

Der Docker Daemon wird normalerweise durch das Host-Betriebssystem gestartet.

**Docker Client** <br> 
* Docker wird über die Kommandozeile (CLI) mittels des Docker Clients bedient
* Kommuniziert per HTTP REST mit dem Docker Daemon

Da die gesamte Kommunikation über HTTP abläuft, ist es einfach, sich mit entfernten Docker Daemons zu verbinden und Bindings an Programmiersprachen zu entwickeln.

**Images** <br> 
* Images sind gebuildete Umgebungen welche als Container gestartet werden können
* Images sind nicht veränderbar, sondern können nur neu gebuildet werden.
* Images bestehen aus Namen und Version (TAG), z.B. *ubuntu:16.04.* 
    * Wird keine Version angegeben wird automatisch :latest angefügt.

**Container** <br> 
* Container sind die ausgeführten Images
* Ein Image kann beliebig oft als Container ausgeführt werden
* Container bzw. deren Inhalte können verändert werden, dazu werden sogenannte *Union File Systems* verwendet, welche nur die Änderungen zum original Image speichern.

**Docker Registry** <br> 
* In Docker Registries werden Images abgelegt und verteilt

Die Standard-Registry ist der Docker Hub, auf dem tausende öffentlich verfügbarer Images zur Verfügung stehen, aber auch "offizielle" Images.

Viele Organisationen und Firmen nutzen eigene Registries, um kommerzielle oder "private" Images zu hosten, aber auch um den Overhead zu vermeiden, der mit dem Herunterladen von Images über das Internet einhergeht. 

