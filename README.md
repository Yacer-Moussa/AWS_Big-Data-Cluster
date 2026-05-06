# AWS EMR & Big Data – Projektübersicht

## Kurzbeschreibung

Im Rahmen dieses Projekts habe ich einen **Amazon EMR Cluster** aufgesetzt und genutzt, um Big-Data-Anwendungen auszuführen. Der Zugriff auf die Cluster-Services erfolgte über einen **SSH-Tunnel mit dynamischem Port Forwarding (SOCKS Proxy)**, wodurch interne Weboberflächen wie Apache Zeppelin sicher erreichbar waren.

---

## Technische Umsetzung

* Aufbau einer Verbindung zum EMR-Master-Node über SSH:

  * Verwendung eines **.pem Key Pairs** zur Authentifizierung
  * Einrichtung eines **dynamischen SSH-Tunnels** (`-D 8157`)
* Konfiguration eines **SOCKS5-Proxys** im Browser (FoxyProxy), um auf interne Webservices zuzugreifen
* Zugriff auf Big-Data-Tools wie:

  * Apache Zeppelin (Notebook-Umgebung)
  * Hadoop Resource Manager
  * Spark UI

---

## Verwendete AWS-Services

* **Amazon EMR** – Verwaltung von Hadoop-/Spark-Clustern
* **Amazon EC2** – Bereitstellung der Cluster-Knoten
* **Amazon S3** – Speicherung und Verarbeitung großer Datenmengen

---

## Wichtige Konzepte

* Secure Shell (SSH) & Key-basierte Authentifizierung
* Port Forwarding / SSH-Tunneling
* SOCKS Proxy & Netzwerkrouting
* Verteilte Datenverarbeitung (Big Data)
* Cloud Computing mit AWS

---

## Herausforderungen & Lösungen

* **SSH Connection Timeout**
  → Lösung: Anpassung der Security Groups (Port 22 freigeben)

* **Proxy blockiert Internetzugriff**
  → Lösung: Selektive Proxy-Regeln in FoxyProxy

* **Fehlerhafte Key-Pfade**
  → Lösung: Verwendung absoluter Dateipfade unter Windows

---

## Ergebnis

Erfolgreiche Einrichtung einer sicheren Verbindung zu einem Cloud-basierten Big-Data-Cluster sowie Nutzung verteilter Datenverarbeitungstools über Webinterfaces.

---
