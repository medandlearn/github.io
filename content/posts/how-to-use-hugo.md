---
title: "How to Use Hugo"
date: 2020-10-15T22:41:02+02:00

toc: true
images: 
tags: 
  [
    "hugo", 
    "git", 
    "choco", 
    "markDown"
  ]
---
## Blogseiten mit hugo erstellen
[mehr über mich](/about)
### Was ist hugo
Mit hugo.js lassen sich statische Webseiten erzeugen. Dies ist ideal um einen Blog darzustellen. 
### Start ins Bloggen
Für euren Start mit einem neuen Blog könnt ihr als erstes einen neuen Projektordner anlegen. Da es unser Ziel ist alle Blog-Dateien sauber zu versionieren, starten wir mit der [Installation von git für Windows](https://gitforwindows.org/).
Mit dieser Installation hält auch ein neues Konsolenprogramm Einzug auf deinem Rechner, git bash. Dieses funktioniert sehr ähnlich zur shell in Linux. Die Arbeit hiermit wird dir (evtl. nach etwas Eingewöhnungsschwierigkeiten) die Arbeit mit git erleichtern.

Du kannst übrigens einen Ordner an gewünschter Stelle in Windows anlegen z. B. *projekte* und kannst dann mit rechter Maustaste direkt git bash öffnen und befindest dich dort dann bereits im Ordner projekte.
Hier legst du nun über git bash einen Ordner z. B. *myblog* an und bereitest ihn für die Versionierung mit git vor.
```bash
mkdir myblog
git init
```

### Installation von hugo unter WIndows
Um hugo unter Window zu installieren lässt sich ein Hilfsprogramm nutzen. 

1. Klicke Start und  schreibe “powershell“. In der sich öffnenden Liste gehe mit rechten Mausklick auf 
Windows Powershell und wähle die Option “Als Administrator ausführen.“
2. Kopiere das golgende Script und füge es in die Powershell ein 
```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
und schließe mit ENTER ab.

3. Bestätige den Prompt mit JA und schließe das Powershellfenster und öffne es erneut als Administrator.
4. Mit dem Befehl 

```bash
choco install hugo
```

wird hugo nun installiert.
### Thema hermit
Damit dein Blog schnell im Web präsentiert werden kann, kannst du ein sogenanntes theme für hugo wählen (es gibt ca. 800 Alternativen). Für den Anfang bin ich mit einem sehr einfachen Theme gestartet, dem theme *hermit*. Dieses wird für schnelles und schnörkelloses bloggen empfohlen. 

Dieses Thema verzichtet in der Grundform auf die Einbindung weiterer 3rd-party-tools. 

Es hat eine MIT-Lizenz und darf somit 
* kommerziell
* modifiziert
* verbreitet
* und privat
 
 genutzt werden.
 Der Weg zur Installation befindet sich auf [github](https://themes.gohugo.io/hermit/)

### Konfiguration

Jedes hugo-Theme kommt mit einem Beispiel im Unterordner *exampleSite* 
Diese enthält auch eine Konfigurationsseite *config.toml*. Der Inhalt lässt sich via copy und paste in die *config.toml*-Datei im root-Verzeichnis eures Projektordners übertragen, den ihr dann anpassen könnt.

Hier könnt ihr euch zunächst darauf beschränken den Titel und den Namen der Autor/*in anzupassen.
```md
title = "Mein Blog über dies und das"
[author]
  name = "Tinto Flinko"
```

### Einen neuen Blogartikel ergänzen

### Mit einem github-repository synchronisieren

```bash
gkohl@DESKTOP-I8QMPGP MINGW64 ~/lese-notizen (master)
$  git remote add origin https://github.com/medandlearn/how-use-git-md

gkohl@DESKTOP-I8QMPGP MINGW64 ~/lese-notizen (master)
$ git push -u origin master
```


