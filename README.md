[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/HEAD)
# Summer School: Digitale Methoden der Zeitungsanalyse

Mittwoch, 11. September 2024 - Donnerstag, 12. September 2024  
09:00 - 19:30 Uhr, Zentralbibliothek Zürich, Hermann-Escher-Saal  
https://www.zb.uzh.ch/de/events/summer-school-digitale-methoden-der-zeitungsanalyse  

## Historische Forschung digital: ein Workshop zum Deutschen Zeitungsportal
**Datum:** Donnerstag, 12. September 2024, 13:30 Uhr - 17:00 Uhr  
**Dozierende:** Michael Büchner ([Deutsche Digitale Bibliothek](https://www.deutsche-digitale-bibliothek.de/)), Franziska Fuchs ([Deutsche Nationalbibliothek](https://www.dnb.de/)), Stephanie Nitsche ([Deutsche Nationalbibliothek](https://www.dnb.de/))  

Das [Deutsche Zeitungsportal](https://www.deutsche-digitale-bibliothek.de/newspaper) – ein Subportal der [Deutschen Digitalen Bibliothek](https://www.deutsche-digitale-bibliothek.de/) – ist mit knapp vier Millionen Ausgaben aus über 1.800 Zeitungstiteln, die fast vollständig mit Volltext vorliegen, der größte Anbieter für historische, digitalisierte Zeitungen in Deutschland. Es stellt damit eine wertvolle Quelle für geschichtlich arbeitende Wissenschaften dar.

Ziel des dreistündigen Workshops ist es, den Teilnehmenden einen umfassenden Überblick darüber zu vermitteln, wie das Deutsche Zeitungsportal für die Forschung, insbesondere in den Digital Humanities, genutzt werden kann. Die Teilnehmenden erhalten dazu zunächst eine kurze Einführung in das Deutsche Zeitungsportal, seine Entstehungsgeschichte, die angebotenen Funktionalitäten und die Vielfalt der verfügbaren Inhalte. Anschließend lernen die Teilnehmenden, wie sie die Programmierschnittstelle (API) der Deutschen Digitalen Bibliothek nutzen können, um Datensets aus dem Deutschen Zeitungsportal herunterzuladen. Der Fokus liegt dabei auf der Vermittlung grundlegender Kenntnisse, die es den Teilnehmenden ermöglichen, in Zukunft eigenständig Datenabfragen zu erstellen. Sie lernen die Funktionsweise der Schnittstellen kennen und erfahren, wie sie Abfragen mithilfe der Dokumentation anpassen und erweitern können.

Nach diesem Einblick führen die Teilnehmenden, begleitet vom DNBLab-Team, eine Datenanalyse auf Basis der gemeinsam heruntergeladenen Daten durch. Hierfür werden Jupyter Notebooks mit Python-Programmcode genutzt. Durch das gemeinsame Live-Coding werden auftretende Fragen und Probleme direkt und interaktiv gelöst. Am Ende werden die gemeinsam analysierten Daten in geeigneten Visualisierungen dargestellt, die Aufschlüsse über die Datenzusammensetzung und mögliche Forschungsansätze geben.

### Programm

| Uhrzeit | Programmpunkt                                                                    | Notebook   | Dozierende   |
|---------|----------------------------------------------------------------------------------|------------|--------------|
| 13:30   | Einführung ins „Deutsche Zeitungsportal“                                         |            | Michael Büchner |   
| 13:45   | Download der Zeitungsportaldaten über die API der Deutschen Digitalen Bibliothek | [001_Download_über_API_der_DDB](https://github.com/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/blob/main/001_Download_%C3%BCber_API_der_DDB.ipynb)    | Michael Büchner |   
| 14:45   | Pause                                                                            |                                        |            |
| 15:00   | Einführung ins DNBLab                                                            |            | Franziska Fuchs |   
| 15:15   | Datenanalyse  <br> <ul><li>Text aus ALTO-XML extrahieren</li><li>Worthäufigkeiten analyiseren und visualisieren</li><li>Optional: Kurzer Einblick in Named Entity Recognition</li></ul>                                                               | [002_Alto-XML-Dateien_einlesen_und_Texte_extrahieren](https://github.com/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/blob/main/002_Alto-XML-Dateien_einlesen_und_Texte_extrahieren.ipynb) <br> [003_Worthäufigkeiten_und_Analyse](https://github.com/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/blob/main/003_Worth%C3%A4ufigkeiten_und_Analyse.ipynb) <br> [004_named_entity_recognition](https://github.com/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/blob/main/004_named_entity_recognition.ipynb)    |   Franziska Fuchs und Stephanie Nitsche  |         
| 16:45   | Fragen und Feedback                                                              |                                        |            |
| 17:00   |                                                                                  |                                        |            |

### Tools

[JupyterLab](https://jupyter.org/) kann beispielsweise über die Distribution „Anaconda“ lokal installiert werden. Eine weitere Option ist, die Jupyter Notebooks auf Basis dieses Repositorys mit [Binder](https://mybinder.org/) oder [Google Colab](https://colab.google/) auszuführen.
- Anaconda: https://www.anaconda.com/download/success
- Binder: https://mybinder.org/v2/gh/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/HEAD
- Google Colab: https://colab.research.google.com/github/Deutsche-Digitale-Bibliothek/ddblabs-summer-school-2024/blob/main

### Links
- Python-Bibliothek für die DDB-API: https://pypi.org/project/ddbapi/
- Notebooks, die LLMs nutzen, um NLP-Aufgaben in historischen Zeitungen durchzuführen: https://github.com/ieg-dhr/Notebooks4Historical_Newspapers
