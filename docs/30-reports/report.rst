Report / Newspaper Webscraping 
==================================

**Cum-Ex - der größte Steuerraub der Geschichte**

Abstract
________

Der Begriff Cum-Ex steht heute für den größten Steuerskandal der deutschen Wirtschaftsgeschichte. Weltweit wurden 150 Milliarden Euro Steuergelder unrechtmäßig bezogen, davon etwa 36 Milliarden in Deutschland [#f1]_. Beteiligt waren mehr als 130 Banken, renommierte Steuerrechtskanzleien, Wirtschaftsprüfer und Großinvestoren. Zudem wird Verstrickungen in die Politik sowie Versäumnissen der Behörden nachgegangen. Die Staatsanwaltschaften ermitteln gegen mehr als 1000 Beschuldigte. 

Um die mediale Präsenz des Themas zu analysieren, wurden jeweils drei deutsche (Süddeutsche Zeitung, Abendblatt und Handelsblatt) und drei internationale (BBC, CNN und The Economist) News-Portale im Zeitraum vom 03.03.2021 bis 31.01.2022 ausgewählt. 

In der internationalen Presse wurde keine Erwähnung des Cum-Ex-Skandals gefunden, obwohl sich die Aktivitäten und der daraus resultierende Schaden keineswegs auf Deutschland beschränkten. Alle drei deutschen Nachrichten-Seiten hingegen haben Cum-Ex als Thema immer wieder aufgegriffen, im Durchschnitt alle 4,6 Tage. Mit 28 Nennun-gen am häufigsten wurde „cum-ex-skandal“ genannt, gefolgt von „cum-ex“ (25-mal), „cum-ex-affaire“ (15-mal), „cum-ex-geschäfte(n)“ (10-mal), „cum-ex-steuerskandal“ (6-mal) und „cum-ex-deals“ (4-mal).

Je nach Ausrichtung des Mediums wurde auf unterschiedliche Aspekte des überaus komplexen Themas fokussiert. Am häufigsten und vergleichsweise nüchtern berichtet das Handelsblatt zu Zeugen, Beweisen und Urteilen, aber auch den verursachten wirtschaftlichen Schaden. Die Süddeutsche Zeitung titelt fast ausschließlich zu „Mr. Cum-Ex“ (Hanno Ber-ger), seine Flucht in die Schweiz und eine mögliche Auslieferung nach Deutschland. Im Abendblatt hingegen fällt in fast jedem Titel zu Cum-Ex der Name Olaf Scholz in Zusammenhang mit seinen Aussagen und Erinnerungslücken.

Im Datensatz stehen Webscraping-Dateien weiterer News-Portale unterschiedlichster Ausrichtung (insgesamt 49, davon wurden 6 analysiert) inklusive der vollständigen Newseinträge zur Verfügung und somit Potenzial, die Analyse noch breiter und tiefer aufzustellen.


1. Einleitung
_____________

Der Begriff Cum-Ex steht heute für den größten Steuerskandal der deutschen Wirtschaftsgeschichte. Nach Schätzung von correctiv.org wurden weltweit 150 Milliarden Euro Steuergelder gestohlen, davon etwa 36 Milliarden in Deutschland [#f1]_. Mehr als 130 Banken waren beteiligt, ebenso wie renommierte Steuerrechtskanzleien, Wirtschaftsprüfer und Großinvestoren. Verstrickungen in die Politik sowie Versäumnissen der Bundesanstalt für Finanzdienstleistungsaufsicht (BaFin) und des Bundesfinanzministeriums (BMF) wird nachgegangen. Die Staatsanwaltschaften ermitteln gegen mehr als 1000 Beschuldigte.

**Doch wie funktionierte diese Betrugsmasche?**

Bei Cum-Ex-Geschäften (auch Dividendenstripping) handelt sich um Aktiengeschäfte, die sich am Tag der Dividendenausschüttung beziehungsweise kurz davor oder danach abspielen. Eine Dividende ist eine Beteiligung der Investoren am Gewinn des Unternehmens, an dem sie Aktien halten. Von diesem Gewinn behält der Staat Kapitalertragssteuer (in Deutschland 25%) ein. Der Investor erhält von seiner Bank eine Steuerbescheinigung, die darüber informiert, dass sich die Aktie zum Zeitpunkt der Dividendenausschüttung im Depot des Investors befand. Mit dieser Steuerbescheinigung kann der Investor einen Teil oder sogar die gesamte Kapitalertragssteuer [#f2]_, die das Unternehmen vorher abgeführt hat, zurückerstattet bekommen. Durch terminierte Leerverkäufe gehört das Aktienpaket jedoch im Zeitraum der Dividendenausschüttung gleichzeitig mehreren Investoren. Damit haben alle Parteien Anspruch auf eine Steuerrückerstattung, obwohl die Steuer auf den Gewinn nur einmal gezahlt wurde. Der einzige Zweck dieser Aktienverkäufe ist es, Steuerbescheinigungen zu erzeugen [#f1]_ und damit Steuern erstattet zu bekommen, die nie bezahlt wurden.

Banken, Anwälte und Investoren behaupteten lange, legal gehandelt und lediglich Steuerschlupflöcher genutzt zu haben. Ein erstes Gerichtsurteil im März 2020 gegen zwei britische Börsenhändler stuft die Cum-Ex-Deals jedoch als Steuerhinterziehung und somit als Straftat ein [#f3]_.

Obwohl erste Fälle bereits in den 90er Jahren bekannt wurden und Whistle Blower 2009 eindringlich vor einem Cum-Ex-Boom warnten, reagiert man erst 2012 mit einer gesetzlichen Neuregelung, die Cum-Ex-Geschäfte mit Leerverkauf unterbinden soll.

Seitdem taucht das Thema Cum-Ex immer wieder in den Medien auf. Untersuchungsausschüsse versuchen, Licht in das kriminelle Netzwerk zu bringen, neue Details und Akteure werden bekannt und weitere Gerichtsverfahren eröffnet.

**Forschungsfragen:**

- Welche Online- Plattformen und Zeitschriften haben im Zeitraum vom 01.04.2021 bis zum 31.01.2022 zum Thema „Cum-Ex“ berichtet und wie oft? 

- Welche Schwerpunkt-Themen wurden aufgegriffen und lassen sich Unterschiede zwischen nationaler und internationaler Berichterstattung feststellen?


2. Daten und Methoden
_____________________

**Daten-Grundlage:**

Der Datensatz wurde durch Marcel Hebing  als Download zur Verfügung gestellt. Im Zeitraum vom 03.03.2021 bis 04.02.2022 (339 Tage) wurden mittels Webscraping täglich automatisiert die Startseiten von 49 ausgewählten Onlinenews-Portalen komplett als html-Datei heruntergeladen und gespeichert. Im Datensatz vertreten sind sowohl deutsche als auch internationale Portale in englischer Sprache. Neben großen Tageszeitungen sind Porle mit Fokus auf Wirtschaftsthemen, Literatur, Informatik oder Wissenschaft enthalten. Eine Auflistung aller Portale ist in der Readme-Datei enthalten.

Weiterhin wurde täglich eine Log-Datei im csv-Format erstellt, die Daten zu den gescrapten Websites enthält, den Download-Status (Status 200 = erfolgreicher Download), Informationen zum Encoding sowie unter „file_name“ den Namen, unter dem die gescrapte html-Datei abgelegt wurde.

**Daten-Selektion:**

Um eine Vergleichbarkeit zu gewährleisten, wurden jeweils drei deutsche und drei internationale Portale ausgewählt. Jeweils zwei große Tageszeitungen wurden mit einem Presseportal mit wirtschaftlicher Ausrichtung kombiniert. In die Analyse wurden die Süddeutsche Zeitung, das Abendblatt und das Handelsblatt als nationale sowie BBC, CNN und The Economist als internationale Presse-Portale aufgenommen (gesamt: 2.033 Dateien). Betrachtet wurde der Zeitraum vom 03.03.2021 bis zum 31.01.2022, insgesamt 335 Tage.

**Fehlende Daten / Kodierungsprobleme:**

Anhand der Status-Codes wurde überprüft, ob für die betrachteten News-Portale Fehler beim Download (status != 200) in den log_csv Dateien verzeichnet wurden. Es wurde lediglich eine defekte Datei gefunden und gelöscht (The Economist vom 08.03.2021). Insofern ist der Datensatz nahezu vollständig.

Bei den Dateinamen für die Economist Downloads wurde in den csv-Dateien eine Inkonsistenz in der Benennung erkannt (Freizeichen hinter ‚economist‘ bei 286 von 339 Dateien) und durch Inkludieren beider Schreibweisen behoben. Da die Zeitung keine relevanten Artikel zu Cum-Ex enthielt, wurde auf ein Umbenennen dieser Dateinamen verzichtet.

**Daten-Transformation:**

Im ersten Schritt wurden die html-Dateien geparst, um alle html-Formatierungen zu entfernen. Weiterhin wurde der Text um störende Zeichen und Stoppwörter bereinigt und damit in eine Liste aussagekräftiger Wörter umgewandelt. Diese Wortlisten wurden im letzten Schritt auf ‚Cum-Ex‘ in unterschiedlichen Schreibweisen durchsucht und alle Nennungen mit Anzahl und „file_name“ als „wordcount_data“ in der SQLite Datenbank zur weiteren Analyse gesichert.

Weiterhin wurden die Überschriften der nationalen Portale (Süddeutsche Zeitung, Handelsblatt und Abendblatt) nach ‚Cum-Ex‘-Nennungen gefiltert. Die gefundenen Überschriften mit dazugehörigem „file_name“ wurden separat nach News-Portal im Data-Warehouse gesichert.

**Daten-Speicherung: SQLite**

Die bereinigten und transformierten Daten wurden zur weiteren Analyse in eine SQLite-Datenbank überführt.  Eine Qualitätssicherung stellt Vollständigkeit und Richtigkeit sicher.


3. Ergebnisse
_____________

Gegenstand der Betrachtung waren sechs News-Portale im Zeitraum vom 03.03.2021 bis zum 31.01.2022 (insgesamt 335 Tage). Es wurden je drei Portale für den deutsch-sprachigen Raum (Süddeutsche Zeitung, Abendblatt und Handelsblatt) und drei der internationalen Berichterstattung (CNN, BBC und The Economist) selektiert. Bei der Auswahl handelt es sich jeweils um zwei große Nachrichtenportale mit allgemeiner Ausrichtung und eins mit Schwerpunkt auf Wirtschafts-Themen.

Zunächst wurden die ausgewählten Plattformen auf den Begriff „Cum-Ex“ in unterschiedlichen Schreibformen durchsucht. Mit 28 Nennungen am häufigsten wurde „cum-ex-skandal“ genannt, gefolgt von „cum-ex“ mit 25 Nennungen, „cum-ex-affaire“ (15mal), „cum-ex-geschäfte(n)“ (10mal), cum-ex-steuerskandal (6mal) und cum-ex-deals (4mal). Weitere Mehrfach-Nennungen gab es für die Begriffe „cum-ex-ausschuss“, „cum-ex-verfahren“, „cum-ex-strafprozess“ und „cum-ex-ermittlungen“.

Im betrachteten Zeitraum von 335 Tagen wurde an 72 Tagen zu „Cum-Ex“ berichtet, also im Durchschnitt alle 4,6 Tage.

.. image:: /images/cum-ex_all_media.png
 
*Abbildung 1:*  Cum-Ex Nennungen im Zeitraum vom 03.03.2021 bis 31.01.2022, kumuliert über alle betrachteten Online-Plattformen (Süddeutsche Zeitung, Handelsblatt und Abendblatt).	

Wie in Abbildung 1 zu sehen, war das Thema im gesamten Zeitraum präsent und wurde immer wieder aufgegriffen. Lediglich im Juni und im September 2021 ist ein Rückgang der Meldungen im Zusammenhang mit „Cum-Ex“ zu sehen.

Über den gesamten Zeitraum haben weder CNN noch BBC oder The Economist als Vertreter der internationalen Medien über den Cum-Ex-Skandal berichtet. Um Fehler bei der Analyse auszuschließen, wurde das Ergebnis durch Überprüfung der Schreibweise in englisch-sprachigen Medien und Suchanfragen zum Begriff Cum-Ex in den drei Portalen verifiziert.

Alle drei deutschen Medien-Plattformen hingegen haben wiederholt berichtet. Im Handelsblatt wurden 61 Nennungen zu „cum-ex“ gefunden, gefolgt vom Abendblatt mit 47 und der Süddeutschen Zeitung mit 30 Nennungen.

.. image:: /images/cum-ex_per_newspaper.png
 
*Abbildung 2:*  Cum-Ex Nennungen im Zeitraum vom 03.03.2021 bis 31.01.2022, differenziert nach Online-Plattform (Süddeutsche Zeitung, Handelsblatt und Abendblatt).


Wie in Abbildung 2 zu sehen, wurde das Thema Cum-Ex in allen drei deutschen Medien über den gesamten Zeitraum immer wieder aufgegriffen. Es fallen einige Zeiträume auf, in denen alle News-Portale gleichzeitig verstärkt berichtet haben:

| Kalenderwoche 13 bis 15 (29.03.2021 - 18.04.2021)
| Kalenderwoche 30 bis 32 (26.07.2021 - 15.08.2021)
| Kalenderwoche 36 bis 38 (05.09.2021 - 25.09.2021)

Die folgende Abbildung 3 listet  alle Überschriften aufsteigend nach Datum und mit dem zugehörigen News-Portal auf, die „cum-ex“ enthalten:

.. image:: /images/header.png

*Abbildung 3:*  Überschriften zum Thema Cum-Ex im Zeitraum vom 03.03.2021 bis 31.01.2022 auf den 
betrachteten Online-Portalen (Süddeutsche Zeitung, Handelsblatt und Abendblatt).

Das Handelsblatt fokussiert in seiner Berichterstattung vor allem auf die tatsächliche Aktenlage, eröffnete Gerichtverfahren und Urteile. Das Abendblatt benennt auffallend häufig Olaf Scholz in Verbindung mit Cum-Ex und der Warburg-Bank. Auch die Erinnerungslücken des Olaf Scholz dienen mehrfach als Titel. Bei der Süddeutschen Zeitung drehen sich fast alle Überschriften um Mr Cum-Ex (Hanno Berger), dessen Verurteilung, Flucht in die Schweiz und seine Auslieferung. 


4. Diskussion
_____________

Bereits die Analyse der häufigsten „Cum-Ex“-Begriffe macht deutlich, es handelt sich um einen Steuerskandal von erheblichem Ausmaß und strafrechtlicher Relevanz. Sowohl die Süddeutsche Zeitung als auch das Abendblatt als Vertreter der großen deutschen Nachrichtenportale sowie das Handelsblatt mit wirtschaftspolitischem Fokus berichteten regelmäßig zum Cum-Ex-Skandal. 

Neben Deutschland , das mit 36 Milliarden Euro den größten Schaden durch illegale Cum-Ex-Geschäfte erlitten hat, waren auch weitere Länder, wie Frankreich (33,4Mrd.), die Niederlande (27Mrd.), Spanien (18,9Mrd.), Italien (13,3 Mrd.) sowie außerhalb der EU die Schweiz und die USA betroffen [#f1]_. Dennoch findet sich in der internationalen Presse über den gesamten Zeitraum kein Beitrag zu Cum-Ex. Um die komplett fehlende Wahrnehmung des Themas in den internationalen News-Portalen einordnen zu können, wäre eine tiefere Analyse über weitere Portale notwendig.

Bei der Analyse der deutschen Portale wurde zunächst davon ausgegangen, dass sich Spitzen in der Berichterstattung mit bestimmten Ereignissen in Zusammenhang bringen lassen, wie etwa Strafanträge oder Gerichtsurteile. Anhand der Überschriften lässt sich jedoch erkennen, dass die unterschiedlichen News-Portale vor allem auf unterschiedliche Aspekte und Personen in der Cum-Ex-Affäre abzielen und diese immer wieder in ihrer Berichterstattung benennen. 

Am häufigsten und vergleichsweise nüchtern berichtet das Handelsblatt. Hier steht im Mittelpunkt, welche Beweise erbracht, welche Zeugen gehört und welche Urteile gefällt wurden, aber auch der wirtschaftliche Schaden, den Cum-Ex verursacht hat. Die Süddeutsche Zeitung titelt fast ausschließlich zu „Mr. Cum-Ex“, seine Flucht in die Schweiz, wie er sein Gold in die Schweiz gebracht hat oder seine Auslieferung nach Deutschland. Es handelt sich dabei um Hanno Berger, ein deutscher Anwalt, der als geistiger Vater und Strippenzieher im Cum-Ex-Skandal gilt. Im Abendblatt hingegen fällt in fast jedem Titel zu Cum-Ex der Name Olaf Scholz. Es ist von seinen Aussagen und immer wieder von seinen Erin-nerungslücken die Rede. Weiterhin fällt in diesem Zusammenhang der Name Peter Tschentscher (damals Finanzsenator) und der der Hamburger Privatbank MM Warburg. Scholz wird vorgeworfen, 2016 als damaliger Bürgermeister von Hamburg Einfluss auf die steuer-liche Behandlung der Warburg-Bank genommen zu haben, indem  auf die Rückforderung von 47 Millionen unrechtmäßig erstatteter Kapitalertragssteuern verzichtet wurde. Das Thema ist hoch brisant und aktuell, denn am 17.02.22 titelte der Spiegel [#f4]_, dass gegen Scholz und Tschentscher Strafanzeige wegen Beihilfe zur Steuerhinterziehung erstattet wurde. 

Zusammenfassend lässt sich sagen, dass das Thema Cum-Ex äußerst komplex und in seinen Mechanismen und beteiligten Personen schwer zu erfassen ist. Insofern ist es nachvollziehbar, dass Medien sich jeweils nur einzelnen Aspekten des Themas Cum-Ex widmen- zum einen um gut recherchierten und inhaltlich korrekten Content zu bieten, zum anderen aber auch, um den Leser nicht zu überfordern. Je nach Ausrichtung des Mediums unterscheiden sich dabei die Themenschwerpunkte.

Der vorliegende Datensatz beinhaltet Daten von 49 News-Portalen, von denen lediglich 6 Portale analysiert wurden, woraus sich weiteres Analyse-Potenzial erschließt. Darüber hinaus liegen die kompletten Websites als html-Files vor inklusive der Berichts-Texte zu den Überschriften, beigefügten Bildern, Videos und Verlinkungen. Für eine inhaltlich tiefere Analyse können auch diese Daten extrahiert, gefiltert und ausgewertet werden.




.. rubric:: Literaturverzeichnis und Quellen

.. [#f1] CORRECTIV. (07. 02. 2022). Correctiv.org. Abgerufen am 07. 02. 2022 von https://correctiv.org/top-stories/2021/10/21/cumex-files-2/
.. [#f2] Kurz, I. (14. 01. 2020). EVERGREEN Youtube Channel. Abgerufen am 07. 02. 2022 von https://www.youtube.com/watch?v=heXS_5Rj8l8
.. [#f3] Legal Tribune Online. (28. 07. 2021). Abgerufen am 07. 02. 2022 von https://www.lto.de/recht/kanzleien-unternehmen/k/bgh-1str51920-erstes-urteil-cum-ex-deals-steuerhinterziehung-revision-warburg-boersenhaendler-strafprozess/
.. [#f4] Siemens, A., & Latsch , G. (17. 02. 2022). Spiegel. Abgerufen am 18. 02. 2022 von https://www.spiegel.de/panorama/justiz/cum-ex-affaere-um-warburg-bank-strafanzeige-gegen-kanzler-scholz-und-buergermeister-tschentscher-a-b5abc953-46cd-49ef-b7d0-184829e31ba1