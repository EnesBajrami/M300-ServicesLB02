# **Modul 300 LB1 Dokumentation** 

# Inhaltsverzeichnis
  - [01 - Umgebung](#01---umgebung)
  - [02 - Verwendetet Tools](#02---verwendetet-tools)
  - [03 - Lernumgebung](#03---lernumgebung)
  - [04 - Wissenstand](#04---Wissenstand)
    - [04.1 - Linux](#04.1---linux)
    - [04.2 - Virtualisierung](#04.2---virtualisierung)
    - [04.3 - Vagrant](#04.3---vagrant)
    - [04.4 - Versionverwaltung/Git](#04.4---versionverwaltunggit)
    - [04.5 - Markdown](#04.5---markdown)
    - [04.6 - Systemsicherheit](#04.6---systemsicherheit)
	
	
  - [05 - Lernschritte & Durchführung](#05---lernschritte & Durchführung)
    - [05.1 - Docker-Befehle](#05.1---Docker-Befehle)
    - [05.2 - SSH-Tunnel](#05.2---SSH-Tunnel)
  - [06 - Ausgeführte Projekte](#06---Ausgeführte Projekte)





## 01 - Umgebung
* VirtualBox 6.0
* (Vagrant)
* Visualstudio-Code
* Git-Client (Git-Kraken)
* SSH-Key für Client wurde erstellt

## 02 - Verwendetet Tools
* Virtualbox 6.0
* Docker Desktop
* Docker Linux
* Docker Compose
* Visual Studio Code
* Git-Client (SSH-Key)


## 03 - Lernumgebung
* GitHub Account wurde bereits ertellt, da es bereits in der LB01 gebraucht wurde
* Git-Client wurde verwendet, sprich mit den verschiedenen Befehlen (git status)
* Dokumentation wurde als Mark Down erstellt (read.me)
* Visualstudio-Code als MarkDown Editor verwendet
* Markdown ist strukturiert, siehe Inhaltsverzeichnis



## 04 - Wissenstand
### 04.1 - Linux
 Da ich im Betrieb sehr viel zu tun habe mit diversen Linux-Server, bin ich im Thema Linux sehr gut unterwegs. Ich habe schon Erfahrungen gesammelt mit DHCP, DNS und Web-Server. Da wir im Geschäft hauptsächlich mit Virtuellen Maschinen arbeiten, sprich ESXi-Server und Vmware Web-Client schon diverse Projekte hatte. Aber ich bin mir jetzt sehr wohl bewusst für was die einzelnen Softwares für eine Funktion haben und wieso es so wichtig ist für die Systemsicherheit, falls dein PC verloren geht SSD/HDD abstürzt trotzdem immernoch im GIT Repository drauf ist. 

### 04.2 - Virtualisierung
Erfahrung in Virtualisierung mit ESXi, VMware und Virtual Box. Server Umgebungen Virtualisierung im Betrieb geplant und ausgeführt. 

### 04.3 - Vagrant
Diverse Vorkenntnisse aus Modul 300 - LB1, Web- und Datenbankserver, FTP-Server und ein DHCP-Server mit Vagrant selbständig erstellt. 

### 04.4 - Versionverwaltung
Erfahrung im Betrieb mit Versionverwaltung Document Management Systemen und Cloud. Mit GitHub noch wenige Erfahrungen gemacht. Ausserdem wurde es bereits auch bei LB01 gebraucht. 

### 04.5 - Markdown
Vorkenntnisse uas Modul 300 - LB1 vorhanden, ganze Dokumenation mit Mark Down geschrieben und auf meinem GIT-Repository veröffentlicht. 

### 04.6 - Systemsicherheit
Diverse Firewalls bereits im Betrieb konfiguriert angepasst etc. In unserem Geschäft benutzen wir die Linux basierte Firewall Barracuda, die jedoch kostenpflichtig ist, die Konfiguration wird alles im Web-GUI erstellt. Jedoch musste ich bei anderen Umgebung eine eigen Firewall einrichten und eine Planung erstellen für die Systemsicherheit im Geschäft, sowie in der Schule. Im Betrieb musste ich diverse Firwalls aufsetzen und konfigurieren, bis zur Firewalls mit Grafischer Obefläche (OPNsense usw.) aber auch Firewalls nur auf CML Basis. Ich musste eine Firewall erstellen mit einer Linux Gentoo VM und dort mussten die Firewall-Rules alles Manuell eingegeben werden, was ziemlich mühsam war, aber jedoch sehr profitieren konnte da ich so besser verstanden habe wie eine Firewall wirklcih funktioniert. Ausserdem habe ich mir die Sache sehr erleichtert indem ich ein Skript geschrieben habe, wo dort alles Reglen bereits aufgeschrieben sind, somit haben ich ein besseren Überblick gehabt. 
Aber ich bin mir jetzt sehr wohl bewusst für was die einzelnen Softwares für eine Funktion haben und wieso es so wichtig ist für die Systemsicherheit, falls dein PC verloren geht SSD/HDD abstürzt trotzdem immernoch im GIT Repository drauf ist. 

### 04.7 - Containersierung
Bisher noch garkeine Erfahrungen mit Containersierung, das ganze Thema ist für mich Neuland. 

### 04.8 - Docker Desktop
Bisher noch garkeine Erfahrungen mit Docker Desktop, das ganze Thema ist für mich Neuland. 

### 04.8 - Micro Services 
Bisher noch garkeine Erfahrungen mit Micro Services, das ganze Thema ist für mich Neuland.






## 05 - Lernschritte & Durchführung

### 05.1 - Docker-Befehle

**Befehle**

  *docker ps -all* - Zeigt alle Aktiven oder beendeten Container an
  *docker images -a* - Zeigt alle lokalen Images an. 
  *docker rm [Containername]* - Löscht spezifischen Container.
  *docker rmi [Imagename]* - Löscht spezifischen Image. 
  *docker pull [Filename]* - Beliebiges Image herunterladen, z.B. Ubuntu/xenial64
  *docker volume create [name]* - Erstellen eines Volumens auf dem Host. 
  *docker inspect [volumename]* - Zeigt detailierte Informationen zum erstellten Volume an. 
  *docker build -t hoi* - Erstellt ein Image aufgrund des Dockerfiles im aktiven Verzeichnis und benennt es mit "hoi". 

 
### 05.2 - SSH-Tunnel

Eine SSH-Verbindung kann mit dem Server augebaut werden indem man den Befehl vagrant ssh (vm-name) eingibt. So kann man direkt 
vom Git-Bash eine Verbindung mit der VM erstellen. Ausserdem habe ich noch im Vagrant-File eine Firewall Rule angegeben, dass eine SSH-Verbindung möglich ist. 

Wenn der SSH-Key erstellt worden ist und im GIT-Hub eingesetzt ist, kann man mit dieswen Befehlen veränderte oder neue Dokumente raufladen. 

Wichtig: Die Befehle müssen innerhalb des lokalen Repositorys ausgeführt werden!

$  cd Pfad\zu\meinem\Repository    # Zum lokalen GitHub-Repository wechseln

$  git status                      # Geänderte Datei(en) werden rot aufgelistet
$  git add -A                      # Fügt alle Dateien zum "Upload" hinzu
$  git status                      # Der Status ist nun grün > Dateien sind Upload-bereit (Optional) 
$  git commit -m "Mein Kommentar"  # Upload wird "commited" > Kommentar zu Dokumentationszwecken ist dafür notwendig
$  git status                      # Dateien werden nun als "zum Pushen bereit" angezeigt
$  git push                        #Upload bzw. Push wird durchgeführt


## 06 - Ausgeführte Projekte






