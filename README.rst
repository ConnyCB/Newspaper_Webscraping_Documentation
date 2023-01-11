Readme 
======
Newspaper Webscraping Project
-----------------------------

**Zeitraum:** vom 03.03.2021 bis 03.02.2022  

**Webscraping-Frequenz:** täglich  

**Extrahiert und zur Verfügung gestellt durch:** Marcel Hebing  

**Folgende News_Portale wurden gescrapt:**

.. csv-table::
   :file: input/portals.csv
   :widths: 5, 20, 65, 10
   :header-rows: 1


Speicherort Original-Dateien
----------------------------

data-lake, "input" Ordner 

**pro Tag:** 

| 49 gescrapte Websites als html-Dateien  
| 1 Log-Datei (csv) mit folgenden Details zum Download:  
  
+---------------+------------+---------------------------------------------+
| name          | Name der Zeitschrift                                     | 
+---------------+------------+---------------------------------------------+
| date          | Datum Download                                           |
+---------------+------------+---------------------------------------------+
| file_name     | Dateiname (zusammengesetzt aus Name der Zeitschrift und  |  
|               | Datum des Downloads)                                     |
+---------------+------------+---------------------------------------------+
| status        | Download erfolgreich= 200, Download fehlgeschlagen= 5++  |
+---------------+------------+---------------------------------------------+
| original_url  | Original URL                                             |
+---------------+------------+---------------------------------------------+
| final_url     | tatsächlich gescrapte URL                                |
+---------------+------------+---------------------------------------------+
| encoding      | Encoding (UTF-8 oder ISO-8859-1)                         |
+---------------+------------+---------------------------------------------+

**Gesamt:**

| 49 News-Portale  
| 339 Tage  
| 16610 Datein  


Speicherort Jupyter Notebooks 
-----------------------------

"notebooks" Ordner

1. newspaper_dwh.ipynb  
 
2. newspaper_analytics.ipynb  


Besonderheiten Selektion und Transformation
-------------------------------------------

**Selektion:**  
 
| Datum: vom 03.03.2021 bis 31.01.2022  
| News-Portale (national): Süddeutsche Zeitung, Handelsblatt und Abendblatt  
| News-Potale (international): CNN, BBC und The Economist  

**Missing Values / Kodierungsprobleme:**    

1 defekte html-Datei gefunden und gelöscht (The Economist vom 08.03.2021)  
Inkonsistenz bei den Dateinamen für die Economist Downloads (Freizeichen hinter ‚economist‘ bei 286 von 339  Dateien)  


Speicherort Analyse-Dateien
---------------------------

dwh,  "output" Ordner

Die Daten wurden in Jupyter Notebook geladen, selektiert, transformiert und in eine SQLite3-Datenbank überführt.  

**Data-Warehouse:**     

- Datei: log_data (Faktentabelle)
    enthält name, date, file_name sowie Download-Status und Encoding     

- Datei: wordcount_data (Dimension)
    enthält Anzahl und Art der cum-ex-Nennungen und den zugehörigen file_name

- Datei: sz_header_df (Dimension)
    enthält alle Überschriften der Süddeutschen Zeitung mit file_name  

- Datei: hb_header_df (Dimension)
    enthält alle Überschriften des Handelsblatt mit file_name  

- Datei: ab_header_df (Dimension)
    enthält alle Überschriften des Abendblatt mit file_name 

JOIN: via file_name 


Möglichkeiten der Analyse
-------------------------

Der Datensatz bietet vielfältige Möglichkeiten, die Berichterstattung von im Zeitraum relevanten Themen zu verfolgen, zwischen den Medien zu vergleichen oder Unterschiede zwischen nationaler und internationaler Berichterstattung herauszuarbeiten.

* Wordcounts
* Filtern nach Suchbegriffen
* Analyse der Überschriften
* Textanalysen
* Bilder und Videos analysieren
* Linkanalysen




