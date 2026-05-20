# Million Song Dataset – Spark SQL und PySpark

In diesem Projekt habe ich mit dem Million Song Dataset in Spark gearbeitet.  
Der Fokus lag darauf, mit Spark SQL, PySpark und grundlegender Datenverarbeitung zu arbeiten.

## Inhalte

- Daten aus dem Million Song Dataset geladen und untersucht.
- Mit Spark SQL Tabellen abgefragt und aggregiert.
- Mit PySpark Segmentdaten verarbeitet.
- Timbre-Werte in Bins eingeteilt.
- Profilvektoren pro Track erstellt.
- Ergebnisse in Spark/Zeppelin kontrolliert.

## Verwendete Techniken

- Spark SQL
- PySpark
- Bucketizer
- Group By, Count, Sum, Case When
- Normierung von Häufigkeiten
- Arbeiten mit Hive-Tabellen

## Ergebnis

Am Ende entstand für jeden Track ein Profilvektor mit den relativen Häufigkeiten der Timbre-Bins.  
Damit kann man Songs besser vergleichen und ihre Lautstärkeverteilung analysieren.

## Screenshots

Die Screenshots zeigen:
- die SQL-Erstellung der Profilvektoren,
- die Ausgabe der berechneten Tabelle,
- und den Spark-Job-Verlauf in Zeppelin.

## Fazit

Das Projekt zeigt praktische Erfahrung mit Spark, Datenaufbereitung und einfacher Feature-Engineering-Pipeline.



# AWS EMR & Big Data – Projekteinstellungen

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
