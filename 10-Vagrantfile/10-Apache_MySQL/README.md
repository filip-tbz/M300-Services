# 10-Apache_MySQL

## Umgebung Vagrant-Cloud

Zuerst müssen wir ins Verzeichnis wechseln und danach die VM starten:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~
            $ cd Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web/

Danach muss die VM vie `vagrant up` gestartet werden:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~/Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web (master)
            $ vagrant up 

## Netzwerkplan

Logischer Plan:

![alt text](https://github.com/tbzsaii/M300-Services/blob/master/00-Images/netzwerkplan.PNG "Netzwerkplan")

Physischer Plan:

Physisch gesehen sind die Firewall, der Proxy und der Server auf dem Laptop. Das heisst, es gibt keine physischen Geräte sondern nur virtuell vorhanden.

## Benutzer und Rechte

In meinem Service wurden zwei Benutzer für je einen Service erstellt. Folgend sehen sie eine Tabelle, mit den Benutzer, Gruppen, Home Verzeichnis und Rechten:

| Benutzer           | Gruppen          | Homeverzeichnis mit Rechten           | 
| ------------------ | ---------------- | ------------------------------------- |
| dbwilliam          | db               | ~/grp/db        r w x                 | 
| webmatt            | web              | ~/grp/web       r w x                 |


## Firewall

Um die `ufw` (uncomplicated firewall) zu installieren, müssen sie folgenden Befehl ausführen: 

`sudo apt-get install ufw -y`

### Regeln

Die Firewall Regeln habe ich so definiert, dass zuerst alle Vogefertigte Regeln abgelehnt werden und neu zwei weitere Regeln hinzugefügt werden. 

`Sudo ufw deny out to any`

`sudo ufw allow from any to any port 22`

`sudo ufw allow from any to any port 80`
