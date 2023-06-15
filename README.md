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
## Fraunhofer-Publica
<a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/publica_list_of_publications_with_attached_files_20230519.xlsx">/.data/publica_list_of_publications_with_attached_files_20230519.xlsx</a></br>
## Fordatis
<a href="https://github.com/antschr96/evaluate_publica_fordatis/blob/main/data/fordatis_bitstream_metadata_20230517.xlsx">.data/fordatis_bitstream_metadata_20230517.xlsx</a>
