# IT2 - Praxisprojekt von Natascha Geisler und Magdalena Kaluza

## Publikation eines kontrollierten Vokabulars mit SkoHub Vocabs


### Einleitung
Kontrollierte Vokabulare sind ein bedeutsamer Bestandteil der Arbeit von Bibliotheken, da sie eine strukturierte Wissensorganisation ermöglichen. Für die technische Umsetzung bieten sich die Tools RDF sowie SKOS an, um die Struktur und den Inhalt zu definieren. Als Basis für das vorliegende Projekt und die Publikation eines kontrollierten Vokabulars mit SkoHub Vocabs wurde die Systematik der des Standorts Köln der Katholischen Hochschulbibliothek gewählt. Aufgrund der Vorteile des Datenstandards erscheint die Anwendung für die Darstellung der Systematik einer wissenschaftlichen Bibliothek als sinnvoll. Zweck ist es, dass das kontrollierte Vokabular die Suche in den spezifischen Wissensgebieten strukturiert und vereinfacht. Hierzu trägt unter anderem die Maschinenlesbarkeit bei. 

### Hierarchie und Beziehungen
Die Systematik dieser Hochschulbibliothek eignet sich aufgrund ihrer hierarchischen Struktur sehr gut für die Erstellung eines Vokabulars. Die Systematik unterteilt die Themengebiete der Sach- und Fachmedien in fünfzig Kategorien und ordnet diesen jeweils Unterkategorien zu. Die Anzahl der Unterkategorien liegt zwischen einer und vierundsechzig Ordnungsbegriffen, was zur Folge hat, dass die Themenbereiche unterschiedlich detailliert systematisiert werden. Die Themengebiete sind den Unterkategorien hierarchisch übergeordnet, während sich die Unterkategorien auf der gleichen hierarchischen Ebene befinden. 

### Festlegung der Begriffe
Eine Bearbeitung der Gesamtsystematik der Katholischen Hochschulbibliothek würde den Rahmen des Projekts sprengen. Aufgrund des unterschiedlichen Umfangs der Themengebiete fiel die Wahl auf das Themengebiet „Sucht“, da sich dieses für die Projektumsetzung eignet.

### Sprache 
Die Systematik der Hochschule Köln ist ausschließlich in deutscher Sprache abgefasst, für die Erstellung des kontrollierten Vokabulars mit SkoHub Vocabs wurde diese jedoch um die englische Sprache erweitert. Dies erscheint für eine wissenschaftliche Hochschulbibliothek, welche auch ausländische Studierende und Forschende zu ihren Nutzer:innen zählt, ein sinnvolles ergänzendes Angebot zu sein.

### Vorgehen in der Projektumsetzungsphase:
Der Austausch in der Kleingruppe fand nicht über ein gemeinsames Kanban Board, sondern mittels Videokonferenzen statt, in denen Aufgabenverteilungen und aufgetretene Probleme und Erfolge direkt besprochen werden konnten. 
Als Grundlage für die Erstellung eines Vokabulars stellte sich die „Einführung in SKOS am Beispiel von Open Educational Resources (OER)“ [^1] von Lohmeier/Pohl/Voß und das integrierte Tutorial als sachdienlich und zielführend heraus. Der grundsätzliche Aufbau eines SKOS-Vokabulars ist nachvollziehbar und verständlich erklärt. 
Die Festlegung einer Basis-Url, sowie die Definition der Identifier und des Vokabulars zu Beginn des Codes sind für die Erstellung wesentlich. Als URL wählten wir die Website der katholischen Hochschulbibliothek, da diese als Quelle des Datensatzes fungiert. Als problematisch stellte sich anfangs die Definition des Vokabulars dar, da diese bei der Validierungsprüfung des Codes als fehlerhaft angezeigt wurde. Dies ließ sich auf das verwendete Element „Date“ zurückführen, auf welches jedoch als nicht verpflichtender Bestandteil des Codes verzichtet werden konnte. Die Unterbegriffe des Vokabulars ließen sich aufgrund der gleichbleibenden hierarchischen Ordnung auf geeignete Weise in der Kleingruppe austeilen. Der Aufbau des Codes gestaltet sich wie folgt: 
1.	Die Notation im Kontext der Klassifikation, sowie die vollständige bevorzugte Bezeichnung des Begriffs der Unterkategorie in deutscher Sprache.
2.	Die Notation im Kontext der Klassifikation, sowie die vollständige bevorzugte Bezeichnung des Begriffs der Unterkategorie in englischer Sprache.
3.	Als allgemeine Notiz wird ergänzt, dass die Inhalte des Vokabulars um ausgedachte Ergebnisse ergänzt wurden, um die verwendeten Quellen klar zu definieren. 
4.	Die Kurzdefinition des Begriffs enthält die Information, dass unter diesem Begriff Medien zum jeweiligen Thema zu finden sind. Dies ist in der konkreten Umsetzung jedoch nicht der Fall, sondern zeigt die Option auf.
5.	Der direkte Oberbegriff, sowie der skos:broaderTransitive.

Als Code ergibt sich so beispielsweise folgende Begriffsdefinition: 

*<Dro/Allgemeine-Literatur> a skos:Concept ;
  skos:prefLabel "Dro/Allgemeine Literatur"@de, "Dro/General literature"@en ;
  skos:broader <Dr/Sucht> ;
  skos:definition "Allgemeine Literatur zum Thema Sucht"@de, "General literature on the subject of addiction"@en ;
  skos:editorialNote "Dieses Beispiel wurde mit ausgedachten Inhalten ergänzt"@de, "This example was supplemented with fictitious content"@en ;
  skos:note: "Dieses Vokabular ist im Rahmen eines Projektes in einem Masterstudiengeang entstanden"@de, "his vocabulary was created as part of a project in a master's degree program"@en ;
  skos:inScheme <> .*
  
Die Definierung der Unterbegriffe funktionierte, als hilfreich konstatierte sich hier die Möglichkeit der Überprüfung und Validierung des Teil-Vokabulars mittels „SKOS testing tool“, was bei entstanden Fehlern (beispielsweise versehentlich gesetzte Leerzeichen) den Bereich des Codes mit der Abweichung eingrenzte. Der Turtle Web Editor trug durch die Verwendung von unterschiedlichen Farben zu der Übersichtlichkeit des Codes und der schnellen Fehlerermittlung bei. Auch zeigte sich hier vor allem die Möglichkeit der Hilfestellung und Absprache in der Kleingruppe als sinnvoll. Nach der erfolgreichen Validierung des Vokabulars musste noch eine Entscheidung über die Visualisierung des Codes getroffen werden. Mithilfe des Tools SKOS Play! konnten verschiedene Visualisierungsoptionen getestet werden. Als am besten geeignet erschien aufgrund der Mehrsprachigkeit des Projekt-Vokabulars die Option „Complete edition – multilingual“.
  
### Lernziele
Durch die Bearbeitung des Projekts hat sich das Verständnis von RDF und SKOS gesteigert, da auf diese Weise die Theorie hinter dem Datenstandard mit der direkten praktischen Umsetzung verknüpft wurde. Das konkrete Anwendungsbeispiel verfestigt das Wissen um den Aufbau des Simple Knowledge Organization Systems, sowie die Regeln des RDF-Modells (Tripel: Subjekt, Prädikat, Objekt).

**Natascha Geissler, Matrikel-Nr: 11111516
Magdalena Kaluza, Matrikel-Nr: 11190642**

 [^1]:Einführung in SKOS (dini-ag-kim.github.io) 



