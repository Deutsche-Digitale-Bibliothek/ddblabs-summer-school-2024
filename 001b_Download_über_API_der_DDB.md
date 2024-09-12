# Summer School: Digitale Methoden der Zeitungsanalyse

*Hinweis:* Diese Markdown-Datei enthält nur die KI-Promps.

## Suchindex newspaper

Ich möchte in Python mit dem Solr-Client pysolr auf den Endpunkt https://api.deutsche-digitale-bibliothek.de/2/search/index/newspaper zugreifen. Kannst Du mir einen Python-Code erstellen, der im Feld location nach „Buenos Aires“ sucht und auch hasLoadedIssues auf „wahr“ setzt. Gibt bitte id, title, location, frequency und progress für jeden Suchtreffer aus.

## Suchindex newspaper-issues

Schreibe ein Python-Code, der mithilfe der pysolr-Bibliothek eine Suche in einem Solr-Index durchführt und die Ergebnisse in ein Pandas DataFrame überführt. Der Solr-Index ist über die URL https://api.deutsche-digitale-bibliothek.de/2/search/index/newspaper-issues erreichbar. Die Suchabfrage soll nach Dokumenten mit der zdb_id „2149754-0“ und dem type „issue“ suchen und bis zu 1000 Ergebnisse zurückgeben. Anschließend sollen die Ergebnisse in ein Pandas DataFrame überführt und angezeigt werden.

## Download der METS/MODS-Daten

Erstelle mit Python ein Verzeichnis La_Otra_Alemania, in dem heruntergeladene XML-Dateien gespeichert werden können. Iteriere durch jede Zeile des bestehenden DataFrames, der die Spalten id und publication_date enthält. Für jede Zeile:
1. Extrahiere den Wert der Spalte id.
2. Formatiere den ISO-DateTime-Wert der Spalte publication_date im Format YYYY-MM-DD.
3. Generiere eine URL https://api.deutsche-digitale-bibliothek.de/2/items/{id}/source/record zur API-Abfrage
4. Setze die HTTP-Header so, dass die Antwort im XML-Format akzeptiert wird.
5. Erstelle einen Dateipfad für die XML-Datei im Format {publication_date}_{id}.xml und speichere sie im erstellten Verzeichnis.

## Download der Bild- und Volltextdaten

Erstelle ein möglichst einfaches Python-Skript, das alle METS/MODS-Dateien in dem Verzeichnis „La_Otra_Alemania“ einliest und URLs mittels des XPath-Ausdrucks `//mets:mets/mets:fileSec/mets:fileGrp[@USE="DDB_FULLTEXT"]/mets:file/mets:FLocat/@xlink:href` extrahiert. Die extrahierten URLs sollen heruntergeladen und in Unterverzeichnissen gespeichert werden. Die Unterverzeichnisse werden nach den Dateinamen der METS/MODS-Dateien benannt. Die heruntergeladenen XML-Dateien sollen mit 1 beginnend durchnummeriert werden.

Das Gleiche soll mit JPEG-Dateien und dem xPath-Ausdruck `//mets:mets/mets:fileSec/mets:fileGrp[@USE="DEFAULT"]/mets:file/mets:FLocat/@xlink:href` gemacht werden.

## DDB-API-Querys

- Liste aller Zeitungstitel im Zeitungsportal als Excel:
[https://api.deutsche-digitale-bibliothek.de/2/search/index/newspaper/select?<br>
q    = hasLoadedIssues:true<br>
wt   = xlsx<br>
fl   = id,title,language,frequency,location,progress,hasFulltext<br>
rows = 2147483647](https://api.deutsche-digitale-bibliothek.de/2/search/index/newspaper/select?q=hasLoadedIssues:true&wt=xlsx&fl=id,title,language,frequency,location,progress,hasFulltext&rows=2147483647)
- Volltextsuche in zwei Zeitungstiteln: 
[https://api.deutsche-digitale-bibliothek.de/search/index/newspaper-issues/select?<br>
df          = plainpagefulltext<br>
q           = Preis*<br>
fl          = id,paper_title,pagenumber<br>
hl          = true<br>
hl.fl       = plainpagefulltext<br>
facet       = true<br>
facet.field = zdb_id<br>
fq          = zdb_id:(2747971-7 OR 2979030-X)](https://api.deutsche-digitale-bibliothek.de/search/index/newspaper-issues/select?df=plainpagefulltext&q=Preis*&fl=id,paper_title,pagenumber&hl=true&hl.fl=plainpagefulltext&facet=true&facet.field=zdb_id&fq=zdb_id:%282747971-7%20OR%202979030-X%29)
