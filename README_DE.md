# **Automotive Diagnostic Intelligence**

## **ECU-Test- und DTC-Analyse \| Power-BI-Portfolio-Projekt**

### **Projektübersicht**

Dieses Projekt demonstriert die Entwicklung einer vollständigen Business-Intelligence-Lösung zur Analyse von Diagnose- und Testergebnissen elektronischer Steuergeräte (ECUs) im Automotive-Bereich mit Microsoft Power BI.

Die Anwendung verarbeitet synthetische Diagnoseereignisse und Testspezifikationen und stellt die Ergebnisse in fünf interaktiven Dashboard-Seiten dar.

Im Mittelpunkt stehen die Überwachung der Diagnosequalität, die Analyse der Spezifikationsabdeckung, der Soll-Ist-Vergleich von Diagnosefehlercodes (DTCs) sowie die Identifikation auffälliger Testfälle und wiederkehrender Fehlermuster.

**Sämtliche verwendeten Daten sind synthetisch und ausschließlich für Demonstrationszwecke erstellt. Es werden keine vertraulichen ECU-Testdaten verwendet.**

### **Eingesetzte Technologien**

* **Microsoft Power BI:** Interaktive Dashboards und Datenvisualisierung  
* **Power Query (M):** Datenimport, Bereinigung, Transformation und Zusammenführung  
* **DAX:** Entwicklung dynamischer KPIs und Kennzahlen  
* **Datenmodellierung:** Tabellenbeziehungen und Filterkonzepte  
* **JSON und Excel:** Synthetische Diagnoseereignisse und Testspezifikationen  
* **Git und GitHub:** Versionsverwaltung und Projektdokumentation

### **Dashboard-Übersicht**

Das Projekt besteht aus fünf Berichtsseiten:

| Seite | Beschreibung |
| ----- | ----- |
| 01 – Diagnostic Overview | Gesamtübersicht über Testfälle, Erkennungsrate und Diagnoseergebnisse |
| 02 – DTC Analysis | Analyse der erwarteten und tatsächlich erkannten Diagnosefehlercodes |
| 03 – Test Case Quality | Spezifikationsabdeckung und Qualitätsbewertung einzelner Testfälle |
| 04 – Root Cause Analysis | Untersuchung wiederkehrender zusätzlicher DTCs und auffälliger Testfälle |
| 05 – Executive Summary | Zusammenfassung der wichtigsten Kennzahlen und Handlungsempfehlungen |

### **Dashboard-Vorschau**

#### **01 – Diagnostic Overview**

#### **02 – DTC Analysis**

#### **03 – Test Case Quality**

#### **04 – Root Cause Analysis**

#### **05 – Executive Summary**

### **Zentrale Kennzahlen**

Die Analyse des synthetischen Datensatzes liefert folgende Ergebnisse:

| Kennzahl | Ergebnis |
| ----- | ----- |
| Analysierte Testfälle | 41 |
| Testfälle mit gültiger Spezifikation | 40 |
| Spezifikationsabdeckung | 97,56 % |
| Erkennungsrate erwarteter DTCs | 95,00 % |
| Testfälle mit fehlendem Soll-DTC | 2 |
| Zusätzliche DTC-Ereignisse | 9 |
| Häufigster zusätzlicher DTC | 0XF90009 |
| Anteil des häufigsten zusätzlichen DTC | 66,67 % |

### **Datenverarbeitung und Analyseprozess**

**1\. Datenimport**

Import synthetischer ECU-Diagnoseereignisse aus einer JSON-Datei und synthetischer Testspezifikationen aus einer Excel-Datei.

**2\. Datenaufbereitung**

Bereinigung und Vereinheitlichung von Testfallkennungen, Diagnosecodes und Datentypen mit Power Query.

**3\. Soll-Ist-Vergleich**

Zusammenführung der Diagnoseereignisse mit den zugehörigen Testspezifikationen anhand der Testfallkennung `TestID`.

**4\. Klassifizierung der Diagnoseereignisse**

Einteilung der Ereignisse in die Kategorien:

* Expected DTC – Erwarteter Diagnosecode erkannt  
* Additional DTC – Zusätzlicher, nicht erwarteter Diagnosecode  
* No Specification Match – Keine passende Spezifikation vorhanden

**5\. Testfallbewertung**

Aggregation der Diagnoseereignisse auf Testfallebene und Ermittlung von Testergebnissen wie `Expected Only`, `Expected + Additional` und `Expected Missing`.

**6\. KPI-Entwicklung**

Berechnung dynamischer Kennzahlen mit DAX, beispielsweise zur Spezifikationsabdeckung und DTC-Erkennungsrate.

**7\. Dashboard-Entwicklung**

Erstellung interaktiver Berichtsseiten mit KPI-Karten, Diagrammen, Detailtabellen und Filtern.

### **Wichtigste Analyseergebnisse**

**Hohe Spezifikationsabdeckung**

40 von 41 Testfällen konnten gültigen Testspezifikationen zugeordnet werden. Die Spezifikationsabdeckung beträgt damit 97,56 %.

**Erkennung erwarteter Diagnosecodes**

Bei 38 von 40 spezifizierten Testfällen wurde der erwartete DTC erkannt. Daraus ergibt sich eine Erkennungsrate von 95,00 %.

**Fehlende Soll-DTCs**

Bei zwei Testfällen wurde der erwartete Diagnosecode nicht erkannt. Diese Fälle sollten hinsichtlich Testbedingungen und Diagnosekonfiguration genauer untersucht werden.

**Wiederkehrende zusätzliche Diagnosecodes**

Insgesamt wurden neun zusätzliche DTC-Ereignisse identifiziert. Der Diagnosecode `0XF90009` trat sechsmal auf und macht damit 66,67 % der zusätzlichen DTC-Ereignisse aus.

Dieses Muster kann auf gemeinsame Testbedingungen oder wiederkehrende diagnostische Auffälligkeiten hinweisen. Eine technische Fehlerursache ist damit noch nicht nachgewiesen.

### **Projektstruktur**

Automotive-Diagnostic-Intelligence/  
├── data/  
│   ├── Synthetic\_DTC\_Events.json  
│   └── Synthetic\_TestSpecification\_Clean.xlsx  
├── powerbi/  
│   ├── Automotive\_Diagnostic\_Public\_Clean.pbip  
│   ├── Automotive\_Diagnostic\_Public\_Clean.Report/  
│   └── Automotive\_Diagnostic\_Public\_Clean.SemanticModel/  
├── screenshots/  
│   ├── 01\_Diagnostic\_Overview.png  
│   ├── 02\_DTC\_Analysis.png  
│   ├── 03\_Test\_Case\_Quality.png  
│   ├── 04\_Root\_Cause\_Analysis.png  
│   └── 05\_Executive\_Summary.png  
├── README.md  
├── README\_DE.md  
└── .gitignore

### **Projekt lokal ausführen**

1. Dieses GitHub-Repository herunterladen oder klonen.  
2. Die Datei `powerbi/Automotive_Diagnostic_Public_Clean.pbip` in Power BI Desktop öffnen.  
3. Den Power-Query-Parameter `pDataFolder` auf den lokalen Pfad des Ordners `data` setzen.  
4. Darauf achten, dass der Ordnerpfad mit einem Backslash (`\`) endet.  
5. Die Änderungen übernehmen und das Datenmodell aktualisieren.  
6. Die fünf interaktiven Dashboard-Seiten öffnen und analysieren.

### **Projektziel und demonstrierte Kompetenzen**

Dieses Portfolio-Projekt verbindet praktische Erfahrungen aus dem Automotive-Testing mit modernen Methoden der Datenanalyse und Business Intelligence.

Es demonstriert insbesondere Kompetenzen in der Aufbereitung technischer Daten, der Entwicklung aussagekräftiger KPIs, der Modellierung von Datenstrukturen und der Visualisierung komplexer Diagnoseergebnisse.

### **Autor**

**Chancel Nouboussi**

Microsoft-Zertifizierungen:

* Microsoft Certified: Power BI Data Analyst Associate (PL-300)  
* Microsoft Certified: Fabric Analytics Engineer Associate (DP-600)  
* Microsoft Certified: Azure Data Fundamentals (DP-900)

GitHub: [https\://github.com/Chancel-Nouboussi](https://github.com/Chancel-Nouboussi)

### **Datenschutzhinweis**

Dieses Projekt wurde unabhängig als Portfolio-Demonstration erstellt und verwendet ausschließlich synthetische Beispieldaten.

Es handelt sich nicht um ein offizielles Projekt eines Automobilherstellers. Die dargestellten Testergebnisse sind fiktiv und dienen der Demonstration von Data-Analytics- und Power-BI-Kompetenzen.

