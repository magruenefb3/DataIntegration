# Tipps für die Verwendung von Pentaho-Funktionen
## Dokumentation
Die Dokumentation der Community Edition ist zu finden unter:  
https://pentaho-public.atlassian.net/wiki/spaces/EAI/overview 

## Gmail-Versand in Pentaho
Zum Versand von Mails mit Gmail ist es zwingend erforderlich ein **App-Passwort** zu erstellen und mittels TLS zu versenden. 
Ein Video zur Erstellung von Passwörtern ist hier zu finden: https://youtu.be/G3OBFqPGXLc?si=y8kQtfmIIRAG5OUE

Ob das App-Passwort für jeden Job neu generiert werden muss, ist unklar. Bitte ggf. melden, falls das so ist.
Die Versandeinstellungen müssen dann folgendermaßen gesetzt werden:

![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/ca6b2f2b-a5fd-46b3-ad0d-7c13369a2693)

width="150" height="100"
Unter "Authentication password" ist dann das App-Passwort einzutragen, das Sie generiert haben.

## Manuelle Erfassung von Werten in einem Grid
Für die manuelle Erfassung von Werten bietet sich das DataGrid (Input) an. Es dient dazu, Werte inklusive der Datendefinitionen manuell zu erfassen.
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/2fdfa688-4f76-474e-9d5a-161b2ca61254)


## Text File Input -- CSV-Dateien laden mit Text File Input
CSV-Dateien enthalten komma-separierte Werte. Statt des Kommas können auch Tabs verwendet werden. In PDI wird dazu **"Textfile" Input** verwendet. 
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/dadc347a-2e02-462b-b2b9-062212a1f122)

Alternativ können CSV-Dateien auch mit "CSV-File Input" geladen werden. Die Funktion ist aber weniger mächtig. 
Textfile Input kann auch verwendet werden, z.B. durch Angabe eines Verzeichnisses **mehrere Dateien in einem Schritt** zu laden. Die Auswahl der Dateien kann auch mit einem regulären Ausdruck erfolgen (s.unten). 

Es besteht auch die Möglichkeit, **Zip-Files**, die CSV-Dateien enthalten zu laden. Für das Laden von Archiven gibt es für den Fall spezieller Archivformate auch eine Funktion zum Öffnen von speziellen Formaten.


## Filtern mit regulären Ausdrücken (regex)
Um z.B. Namen von Dateien zu bestimmen, die geladen werden sollen, können reguläre Ausdrücke verwendet werden. 
Diese können z.B. auf der folgenden Website konstruiert und gegen Text getestet werden: https://regex101.com/ 

## Excel-Dateien
Das Laden von Excel-Dateien kann zu Problemen führen, da Excel z.B. auch mit Zeilenumbrüchen arbeitet (ALT-RETURN), die schwer durch Pentaho zu verarbeiten sind. Auch die Darstellung von Datumswerten stellt ein häufiges Problem dar. Es sollte daher, wenn möglich vermieden werden, mit Excel zu arbeiten und stattdessen vorab aus Excel eine CSV-Datei erstellt werden.
PDI verfügt dennoch über eine Möglichkeit, Excel-Dateien zu laden. (Microsoft Excel Input).


