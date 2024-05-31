# Tipps für die Verwendung von Pentaho-Funktionen

## Gmail-Versand in Pentaho
Zum Versand von Mails mit Gmail ist es zwingend erforderlich ein **App-Passwort** zu erstellen und mittels TLS zu versenden. 
Ein Video zur Erstellung von Passwörtern ist hier zu finden: https://youtu.be/G3OBFqPGXLc?si=y8kQtfmIIRAG5OUE

Ob das App-Passwort für jeden Job neu generiert werden muss, ist unklar. Bitte ggf. melden, falls das so ist.
Die Versandeinstellungen müssen dann folgendermaßen gesetzt werden:

![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/ca6b2f2b-a5fd-46b3-ad0d-7c13369a2693)

Unter "Authentication password" ist dann das App-Passwort einzutragen, das Sie generiert haben.

## Manuelle Erfassung von Werten in einem Grid
Für die manuelle Erfassung von Werten bietet sich das DataGrid (Input) an. Es dient dazu, Werte inklusive der Datendefinitionen manuell zu erfassen.
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/2fdfa688-4f76-474e-9d5a-161b2ca61254)


## CSV-Dateien laden
CSV-Dateien enthalten komma-separierte Werte. Statt des Kommas können auch Tabs verwendet werden. In PDI wird dazu "Textfile" Input verwendet. 
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/dadc347a-2e02-462b-b2b9-062212a1f122)

