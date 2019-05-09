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
	
	
  - [05 - Lernschritte & Durchführung](#05---lernschritte&Durchführung)
    - [05.1 - Docker-Befehle](#05.1---Docker-Befehle)
    - [05.2 - SSH-Tunnel](#05.2---SSH-Tunnel)
  - [06 - Ausgeführte Projekte](#06---Ausgeführte-Projekte)
    - [06.1 - Tutorial](#06.1---Tutorial)
    - [06.2 - Kontrolle](#06.2---Kontrolle)
    - [06.3 - Ausführen eines Containers mit peristente Datenablage](#06.3---AusführeneinesContainersmitperistenteDatenablage)
  [07 - Netzwerkplan Apache](#06---netzwerkplanapache)
    - 07.1 - Docker mit Apache](#07.1---dockermitapache)
    - 07.2 - Testen](#07.2---testen)
  - [08 - Reflexion](#01---Reflexion)
  - [09 - Vergleich Vorwissen/Wissenszuwachs](#01---VergleichVorwissen/Wissenszuwachs)
  - [10 - Kubernetes](#01---Kubernetes)




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
  *docker build -t hallo* - Erstellt ein Image aufgrund des Dockerfiles im aktiven Verzeichnis und benennt es mit "hallo". 

  **Relevante Befehle**

  *docker build -t EnesBajrami/M300-ServicesLB02 .*
  *docker build --tag test1 .*
  *docker push EnesBajrami/M300-ServicesLB02*
  *delete pod to update image*
  *docker image ls*
  *docker ps -all*
  *docker rmi -f imagename*

 
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



### 06.1 - Tutorial


Als aller erstes, damit der Docker Deamon läuft, muss es als Administraotr ausgeführt werden und gestartet werden. Anschliessend als Kontrolle den Befehl "docker run hello-world" eingeben, wenn dieser ohne Komplikationen ausgeführt wurde kann man sich sicher sein, dasss nun docker wirklich läuft. 


    Zuerst wurde ein Verzeichnis (C:/LB2/src) erstellt.
    Mithilfe Visual Studio Code habe ich ein index.php File in /src/ erzeugt und ein Dockerfile direkt in C:/LB2/.
    Das PHP-File besteht aus diessem simplen Code:

  <?php
    echo "hallo-welt"
  ?>

    Um den PHP-Apache Dienst auf Docker laufen zu lassen, suche ich auf der Docker Hub Webseite nach dem offiziellen PHP Image. Folgendes kommt nun ins Dockerfile:

  FROM php:7.3.4-apache = dabei ist es leider nicht mit dieser version gegangen deshalb habe ich eine ältere version genommen sprich 7.0 -apache
  COPY src/ /var/www/html
  EXPOSE 80

FROM: gibt an welches Image heruntergeladen werden soll, in diesem Fall PHP-Apache 7.3.4.
COPY: Kopiert den Inhalt des Host-Verzeichnisses (src/) ins Verzeichnis des Containers (/var/www/html).
EXPOSE: Sagt Docker auf welche Ports die laufenden Container hören sollen.
Das Dockerfile abspeichern und via CMD den Befehl docker build (--tag image101 .) eingeben + ausführen. Dies erstellt ein neues Image mit dem Namen hallo-welt.


### 06.2 - Kontrolle

Als Kontrolle habe ich den Befehl *docker images -a* eingegeben, dieser Befehl zeigt alle Lokalen Images auf den Rechner auf. 

Ausserdem bei jedem Browser den localhost ausprobiert und fertig. 


Das nächste Problem war dieses hier wegen den rechten: 
SECURITY WARNING: You are building a Docker image from Windows against a non-Windows Docker host. All files and directories added to build context will have '-rwxr-xr-x' permissions. It is recommended to double check and reset permissions for sensitive files and directories.



### 06.3 - Ausführen eines Containers mit persistenter Datenablage 

Damit ich den Container nicht bei jeder Änderung im PHP-File stoppen und wieder starten muss, erzeuge ich beim starten des Containers eine persistente Datenablage und jede Änderung die ich am Host im PHP-File vornehme wird auch im Container vorgenommen.

    In der CMD folgenden Befehl eingeben: docker run -p 80:80 -v C:/lb2/src/:/var/www/html/ hallo-welt.  / docker run -p 80:80 hallo-welt


    Leider bekam ich hier eine Fehlermeldung, dass ich keinen Zugriff hätte. Der Fehler war, dass ich im dockerfile "RUN ["chmod", "+x", "/usr/src/app/docker-entrypoint.sh"]" diese Zeile noch hinzufügen musste, damit es executable wird. Anschliessend musste das Image gelöscht werden und neu erstellt werden oder ein neues erstellen. Das image wurde mit dem Befehl "docker rmi hallo-welt" gelöscht, jedoch gab es dort wiederum auch probleme, sprich dort musste ich anschliessend noch ein zusätzliches Parameter eingeben, nämlich "docker rmi -f hallo-welt"

Nun kann man in einem beliebigen Browser mit der Eingabe localhost das index.php-File aufrufen und alle Änderungen auf dem Host sind sofort nach aktualisieren der Seite sichtbar.

    Mit der Tastenkombination CTRL-C in der CMD kann man den Container stoppen.
    Möchte ich den Container erneut starten, lasse ich mir mit docker ps --all alle vorhandenen Container anzeigen und starte diesen wieder indem ich die ersten paar Buchstaben und Ziffern der ID eintippe docker start 565f






## 07 - Netzwerkplan Apache
+---------------------------------------------------------------+
! Container-Engine: Docker                                      !	
+---------------------------------------------------------------+
! Gast OS: Ubuntu 16.04                                         !	
+---------------------------------------------------------------+
! Hypervisor: VirtualBox                                        !	
+---------------------------------------------------------------+
! Host-OS: Windows 10                                           !	
+---------------------------------------------------------------+
! Notebook - Schulnetz 10.x.x.x                                 !                 
+---------------------------------------------------------------+





### 07.1 - Docker mit Apache

Zustäzlich habe ich nochmals ein Web-Server erstellt jedoch mit Apache, hierbei ist anders, dass dort der Ubunut-Server automatisch gepudatet wird und mehr technisches wisse benötigt. 
Sprich das Dockerfile beinhandelt, dass der Serve geupdatet wird und die Konfiguration vom Apache-Server

Zusätzlich wurde ein weiterer Ordner erstellt, der sich web nennt. In diesem Ordner befindet sich eine index.html datei, von dort bekommt dann der Server den HTML-Code für die Darstellung der Webseite. 

Wenn alles bereit ist und richtig konfiguriert wurde, muss als aller erstes ein Image erstellt werden. 

--> Zuerst im CMD mit Admin-Rechten auf das Verzeichnis zugreifen, indem der Dockerfile liegt 
--> Bevor wir zu der Installtion gehen muss als aller erstes der Docker Deamon gestartet werden auch hier zwingend mit Admin rechte. 
--> Anschliessend muss ein Image erstellt werden, dass vom dockerfile herkommt sprich "docker build --tag test1 ."

Docker Container starten:

docker run --rm -d -p 8080:80 -v /web:/var/www/html --name apache test1 = Anschliessend wird ein neuer container erstellt von diesem Image aus. Und der Service läuft. 




### 07.2 - Testen

*docker image ls* = mit diesem Befehl sieht man ob das Image erstellt wurde (test1)
*curl http://localhost:8080* = Hier kann man testen ob der Webserver überhaupt funktioniert, oder einfach im Browser localhost eingeben. Es erscheint der Inhalt der index.html Datei

Das testing hat bei mir beides funktioniert alles ohne Komplikationen. 






## 08 - Reflexion

Anfangs kam ich garnicht mit Docker draus und musste nur für die Installtino und Konfiguratin viel Zeit in anspruch nehmen. Nach den Ferien musste ich wieder das ganze wissen auffrischen und geriet in einer stresssituation. Diverses wollte nicht mehr funktionieren Docker hatte Störungen, virtuelle Maschinen konnten nicht gestartet werden musste alles wieder von neu installieren und Konfigurieren. Bei dem Problem mit der VM musste ich einfach in den Windows-Einstellungen den Dienst Hyper-V aktivieren, aus irgendeinen Grund war dieser bei mir deaktiviert. Docker funktionierte auch nach der Installation nicht und musste wieder dort viel Zeit aufwenden, dass es wieder in Betrieb ist. Beim Docker musste ich einfach bei den Einstellungen die shared drives aktivieren. Auch nachdem wollte docker immer noch nicht laufen es gab immer eine Fehlermeldung das der Docker Deamon, sprich der Dienst nicht läuft, auch dort musste ich wiederum viel Zeit investieren um diesen Fehler zu beheben, anschliessend habe ich einen Artikel gefudnen der sagt, dass man am besten diesen Befehel eingeben muss, damit der Deamon dienst läuft (docker-machine create box) so wird eine Box erstellt. Leider brachte auch hier wiederum ein neuen Fehler, dass hyper v check nicht funktioniert oder ich hyper-v ausschalten soll, doch wenn ich das täte würde docker garnicht funktionieren. Auch dafür habe ich ein Workaround gefunden mit diesem Befehl (--virtualbox-no-vtx-check). auch hier wiederum nur fehler anschliessend fand ich einen Eintrag, dass das ganze Admin rechte bräuchte und es schliesslich funktionierte, trotzdessen kam ich sehr im stress und konnte keine komplexere Themen erstellen, aber bin trotzdessen sehr zufrieden mit mir. 

Ausserdem hatte ich noch schwierigkeiten mit Vagrant, bei einem beispiel von ihnen steht, dass auch mit vagrant und docker zusammen etwas zu erstellen, das ist jedoch leider nicht möglich da docker hyperv benötigt und virtual box geht nur wenn diese entfernt ist.

## 09 - Vergleich Vorwissen/Wissenszuwachs

Vor den Projekt wuste ich noch nichts über docker sprich container usw. allerdings hatte ich diverse schwierigkeiten, die ich überwinden musste aber kann jetzt sagen, dass ich einigermassen docker gut verstehe. Der wissenszuwachs ist enorm. Wenn man bedenkt, dass ich vorher kein plan hatte und jetzt das einigermasesn in Griff habe ist es erstaunlich das alles für mich in dieser kurzen Zeit gelernt zu haben. 

Ich hatte bisher noch nie mit Docker gearbeitet oder davon gehört, hatte zwar diverse schwierigkeiten doch mit einbisschen googlen und youtube Videos ging das ganze schlussendlich doch gut aus.

Ich wusste nicht einmal wie man docker richtig konfigurieren muss und das mann in anfangs starten muss, auch Luafwerke spezifisch anhängen musste. Ich kannte die Befehle nicht usw. 


## 10 - Kubernetes
Kubernetes fasst Container-Images, ihre Konfiguration und die Anzahl der benötigten Instanzen in Deployments zusammen, so der Sprachgebrauch des Orchestrierungssystems. Die Parameter eines Deployments überwacht Kubernetes selbsttätig. Das Tool sorgt dafür, dass die gewünschte Anzahl von Containern jederzeit läuft. Änderungen an der Software oder der Konfiguration verteilt Kubernetes mit einem Rollout. Dieser Prozess lässt sich pausieren, fortsetzen und rückgängig machen (Rollback).

Optimierung der Nutzung der Computer-Ressourcen Kubernetes setzt die Container eines Deployments selbständig dort ein, wo entsprechende Ressourcen frei sind. Der Anwender kann Mindest- und Höchstwerte der Ressourcennutzung (Rechenzeit, Speicherplatz) für die Container festlegen, um dem Orchestrierungstool einen Rahmen vorzugeben.

Zahlreiche Optionen für dauerhafte Datenspeicherung (Persistent Storage)

Container sind zustandslos. Für die dauerhafte Speicherung von Konfigurations- und Nutzerdaten bietet Kubernetes Schnittstellen zu zahlreichen Diensten wie zum Beispiel EBS von Amazon Web Services oder Google Cloud Platform.


