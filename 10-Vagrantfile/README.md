# 10-Vagrantfile

## QuickLink
- [00 Test VM's](https://github.com/tbzsaii/M300-Services/tree/master/10-Vagrantfile/00-Test%20VM)
- [10 Apache MySQL](https://github.com/tbzsaii/M300-Services/tree/master/10-Vagrantfile/10-Apache_MySQL)
- [20 Apache Webserver](https://github.com/tbzsaii/M300-Services/tree/master/10-Vagrantfile/20-Apache%20Webserver)

## Informationen
In diesem Dokument finden sie folgende Informationen zu den Vagrant-Files:
- [Netzwerkplan] (#netzwerkplan)
- [Vagrantbefehle] (#vagrant-befehle)

## Netzwerkplan
Logischer Plan:

![alt text](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/netzwerkplan.PNG "Netzwerkplan")

Physischer Plan:

Physisch gesehen sind die Firewall, der Proxy und der Server auf dem Laptop. Das heisst, es gibt keine physischen Geräte sondern nur virtuell vorhanden.


## Vagrantbefehle

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
