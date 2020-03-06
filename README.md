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
Nach der Installation wurden 3 weitere wichtige Extensions hinzugefügt
  Markdown All in One
  
            Name: Markdown All in One
            Id: yzhang.markdown-all-in-one
            Description: All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
            Version: 2.7.0
            Publisher: Yu Zhang

  Name: Vagrantfile Support
  
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


## Wissenstand
### Linux

### Vagrant

### Virtualisierung

### Git

### Markdown

### Systemsicherheit



### Standard Befehle
Visual Studio Code öffnen:
`code`

Laufende Prozesse anzeigen mit folgenden Optionen:
 `ps faux`
- rudimentäre Baumstruktur (`f`)
- Prozesse anderer Benutzer anzeigen (`a`)
- Besitzer zu jedem Prozess anzeigen (`u`)
- Prozesse anzeigen, die nicht nur aus dem Terminal gestartet wurden (`x`)
 
Verzeichnis wechseln:
`cd [PATH]`

CLI schliessen:
`exit`

### Vagrant Befehle
Server starten:
`vagrant up`

Serverstatus der VM aufzeigen:
`vagrant status`

VM herunterfahren:
`vagrant halt`


## Reflexion

## Links

[Markdown Cheat-Sheet](https://www.markdownguide.org/cheat-sheet/)