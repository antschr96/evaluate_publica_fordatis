# Analyse digitaler Objekte in den Repositorien Fordatis und Fraunhofer-Publica

# Skripte zur Abfrage von Metadaten der Repositorien

## Fraunhofer-Publica
Dieses Skript führt eine Abfrage in der Fraunhofer Publica durch. Das Ergebnis wird darauf hin geparst, ob Dateianhänge zu diesem Dokument verfügbar sind. Falls ja, werden ein paar Daten extrahiert und in eine Datei geschrieben. </br>

Skript: <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/publica_get_items_with_attachements.ipynb"> ./publica_get_items_with_attachements.ipynb</a>
Ausgabedatei: <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/publica_list_of_publications_with_attached_files.csv">./publica_list_of_publications_with_attached_files.csv</a>

## Fordatis
Die Abfrage von Metadaten in Fordatis muss mehrstufig angelegt werden. 
1. Abfrage der Items mit diesem Skript: <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/fordatis_get_items.ipynb">./fordatis_get_items.ipynb</a>
2. Abfrage der bitstreams mit diesem Skript: <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/fordatis_get_bitreams_for_each_item.ipynb">./fordatis_get_bitreams_for_each_item.ipynb</a>

Das erste Skript erzeugt eine Liste der Unique Identifier, die von dem zweiten Skript benutzt wird, um Metadaten der digitalen Objekte (bitstreams) auszulesen.</br>
Das Ergebnis wird in die Datei geschrieben: <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/fordatis_bitstream_metadata.csv">./data/fordatis_bitstream_metadata.csv</a></br>
Die Datei ./data/fordatis_item_metadata.csv wurde nicht weiter ausgewertet, lediglich als Hilfsmittel zur Kontrolle von Datensätzen im Frontend eingesetzt.</br> 

# Analyse Ergebnis: Auswertung der Daten in Excel
Beide Ergebnisdateien enthalten jeweils ein readMe-Datenblatt mit Erläuterungen der Tabellenblätter und Spalten.

## Fraunhofer-Publica
<a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/publica_list_of_publications_with_attached_files_20230519.xlsx">/.data/publica_list_of_publications_with_attached_files_20230519.xlsx</a></br>

## Fordatis
<a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/fordatis_bitstream_metadata_20230517.xlsx">.data/fordatis_bitstream_metadata_20230517.xlsx</a>

# Formatidentifikation mit DROID
Ausgewählte Dateien, deren MIME Type (MIME Type: application/octet-stream) von der Software DSpace beim Upload nicht eindeutig erkannt werden konnte bzw. als Binärinformation interpretiert wurde, wurden näher untersucht. Auffällig ist die Zahl von 127 Dateien, deren MIME Type (MIME Type: application/octet-stream) von der Software DSpace beim Upload nicht eindeutig erkannt werden konnte bzw. als Binärinformation interpretiert wurde. Bei insgesamt 12 digitalen Objekte erfolgte jedoch eine Formatidentifikation beim Upload. Die übrigen 115 digitalen wurden anhand der Dateierweiterung in der Excel-Datei manuell klassifiziert.
Um Erfahrungen mit der Formatidentifikation zu sammeln wurden ausgewählte Dateien mit DROID untersucht:
* 5 Dateien, deren Datenformat nicht erkannt wurde (Dateinamen: xxxx.feather, uniax_simulator_for_microstructure_evolution_40tasks, ebsd.ang, Mesh.inp, Coeff Thermal Expansion_C12A7.dat)
* 2 von 11 npy-Dateien (Dateinamen: test_set_properties.npy, training_set_properties.npy)
* 2 matlab-Dateien (Dateinamen: accln_5Wcr_1ep_10tc.mat), um mehr Informationen zur verwendeten Version zu erhalten.
* 1 SPSS-Datei (Dateiname: Data set_Air travel_Fraunhofer ISE.sav), 1 Pythonprogramm (view_data.py), um Informationen zur Identifikation durch DROID zu erhalten.
* 3 Dateiarchive (Dateinamen: Figure 5.zip, Raw-data_tribometer.7z, macroscopic_testing.zip), um mehr Informationen zur Identifikation der enthaltenen Dateien zu ermitteln.

Das Analyse-Ergebnis von DROID liegt als <a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/droid_analyse_ergebnis.txt"> Report</a> vor.

Als problematisch für eine Archivierung stellten sich ein ausführbares Programm, das von DROID als solches erkannt wurde. Elf binäre Numpy-Dateien und eine weitere Binärdatei konnten auch von DROID nicht identifiziert werden. Die Informationen wurden in der Excel-Datei festgehalten:
<a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/publica_list_of_publications_with_attached_files_20230519.xlsx">/.data/publica_list_of_publications_with_attached_files_20230519.xlsx</a></br>
