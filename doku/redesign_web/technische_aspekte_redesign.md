# Kickoff redesign Web

## Inhalt
- Allgemein technische Tools und Specs
- LF Ticket Webshop
	- Übersicht interne Systeme	
	- Systemaufbau (alt/neu)
	- Komplexität Schnittstellen
	- Anforderungen
	- Vorschlag Architektur
	- Testing / Umgebungen
	- Daten CMS bisher

# Allgemeine technische Tools und Specs

## Tools und Versionen
- Python 3 (.4)?
- Django 1.7?
- github.com
- Datenbank MySQL/InnoDB oder Postgres?
- Entwicklungsumgebung? z. B. pyCharm
- CI Continous Integration Server z. k. Jenkins oder
- CD Continous Delivery Server wie z. B. Wercker?
- sentry (logging Plattform?)
- Webserver: Apache, gunicorn?, nginx static
- Hosting: Amazon EC2, RDS
- JavaScript Frameworks
- webcomponents
- async Technologie für Sitzplatzstatus wie asyncio oder nodejs

# LF Ticket Webshop

In diesem Dokument sollen die wichtigsten Aspekte für die Implementation des Webshop geklärt werden.

## Übersicht interne Systeme und Schnittstellen
![interne Systeme](interne_schnittstellen_systemuebersicht.png)

## Systemaufbau Webshop bisher

![Systemaufbau bisher](systemaufbau_bisher.png)


## Anforderungen

- Ist-Stand
- Excel
- Neue Anforderungen und Verbesserungen

## Komplexität Schnittstellen
Anhand des Use Cases von 2011 wird die Schnittstelle zwischen Webshop und Kreditkarteservice erklärt.

![Systeme beim Ticketkauf](Systeme_beim_Ticketkauf_Online.png)

## Testing Webshop

- Unittest 
- Lasttest mit Apache JMeter
- Automatisierte Functionale Tests mit Selenium Beispiel
- Umgebungen Test, Integration (master), Live
- doctest?
- Sphinx documentation?

## Daten CMS ERM bisher
[ERM](CMS_LF_ER_Modell.pdf)

- Sprachkonzept via tblTexts, tblEntityTypes und tblLanguages

## Verbesserungen zum alten Modell
- tblComposer, tblConductors und tblPerformers sind einzelne Tabellen mit Personen, nun gibt es aber Personen welche Dirigent, Komponist und Künstler/Musiker sind, diese müssen im jetzigen Modell mehrmals erfasst werden. 
- tblEnsemble kann mit Performars bestück werden. Evtl. sollte man tblChoir mit einer ähnlichen Funktion ausstatten, oder man verallgemeinert eine Gruppenhierarchie und typsiert die Gruppen...

