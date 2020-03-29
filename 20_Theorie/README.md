# 25-Benutzer und Rechte

## Inhalt
  - [Benutzer und Rechte](#benutzer-und-rechte)

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
