# 10-Apache_MySQL

## Umgebung Vagrant-Cloud
Zuerst müssen wir ins Verzeichnis wechseln und danach die VM starten:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~
            $ cd Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web/

Danach muss die VM vie `vagrant up` gestartet werden:

            AzureAD+ShagithijanBaasgaran@DESKTOP-B2E99P6 MINGW64 ~/Documents/M300_personal/MeinLokalesRepository/M300-Services/VM/web (master)
            $ vagrant up 


## Benutzer und Rechte
In meinem Service wurden zwei Benutzer für je einen Service erstellt. Folgend sehen sie eine Tabelle, mit den Benutzer, Gruppen, Home Verzeichnis und Rechten:

| Benutzer           | Gruppen          | Homeverzeichnis | Gruppenrechten     | 
| ------------------ | ---------------- | --------------- | ------------------ |
| dbwilliam          | db               | ~/grp/db        | r w x              | 
| webmatt            | web              | ~/grp/web       | r w x              |


## Firewall
Um die `ufw` (uncomplicated firewall) zu installieren, müssen sie folgenden Befehl ausführen: 

`sudo apt-get install ufw -y`

### Regeln
Die Firewall Regeln habe ich so definiert, dass zuerst alle vorgefertigten Regeln abgelehnt werden und neu zwei weitere Regeln hinzugefügt werden. Die Einstellunge für die `ufw` findet ihr folgendermassen:

                vagrant@lxwsrv01:~$ sudo ufw status
                Status: active

                To                         Action      From
                --                         ------      ----
                22                         ALLOW       Anywhere
                80                         ALLOW       Anywhere
                22 (v6)                    ALLOW       Anywhere (v6)
                80 (v6)                    ALLOW       Anywhere (v6)

                Anywhere                   DENY OUT    Anywhere
                Anywhere (v6)              DENY OUT    Anywhere (v6)


### Proxy Einstellungen
Der Proxy wurde konfiguriert und ist einsatzbereit. Die Website ist nun unter folgendem Link erreichbar:

                http://mysql-m300:8080/phpmyadmin/
                
                username: root
                password: m300mysql

### Testfälle
Für diesen Webserver wurden folgende Tests vorgenommen:



