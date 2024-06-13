# Erstellung eines Dashboards in PowerBI

## Voraussetzungen
* Maschine mit aktuellem MS Windows-Betriebssystem

## Vorbereitung
1) Laden Sie die Kindergarten-DB in MySQL --> [Link zum DB-Skript](https://github.com/magruenefb3/DataIntegration/blob/main/Kindergarten-DB/kindergarten-create-schema-and-data.sql) 
2) Installieren Sie PowerBI Desktop über den Store oder über folgenden [Link](https://powerbi.microsoft.com/de-de/downloads/)
3) Melden Sie sich in PowerBI an (M365-Account). 

## Einarbeitung
Arbeiten Sie sich in die Verwendung von PowerBI ein. Eine kurze, zehnminütige, englischsprachige Einführung von Keven Stratvert finden Sie hier auf YouTube: [Einführung in PowerBI](https://youtu.be/NNSHu0rkew8?si=bvksxV-Ac3rA1DPB)

# Aufgaben
## Aufgabe 1: MySQL in PowerBI einbinden
Binden Sie die Kindergarten-DB in PowerBI ein und erzeugen Sie aus der Datenbank ein Datenmodell.  
Achtung: Es kann passieren, dass auf Ihrem Windows-System die Einbindung von MySQL mit den nativen Treibern nicht funktioniert. Installieren Sie dann den MySQL-Unicode-ODBC-Treiber: [Link zum ODBC-Treiber](https://dev.mysql.com/downloads/connector/odbc/)

Klicken Sie dazu auf "Abrufen von anderen Datenquellen":  
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/f3673560-7494-4084-979c-d552461b6101)

Nun öffnen Sie die ODBC-Verbindung zu MySQL. Sollten Sie noch keine ODBC-Verbindung haben, erstellen Sie sich eine. 
Ein Video zur Einrichtung einer ODBC-Verbindung finden Sie [hier](https://youtu.be/oxGQGKIp4Ms?si=ZF72tmqRkMsmq6DX).

Wählen Sie aus dem Dropdown Ihre Verbindung aus:  
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/6453a583-1494-44c8-a690-c37da78d6b51)

Sollte es beim Laden zu Fehlermeldungen kommen, prüfen Sie bitte, ob MySQL im Hintergrund als Dienst gestartet ist. 
Speichern Sie Ihre PowerBI-Lösung, bevor Sie weiterarbeiten.

## Aufgabe 2: Daten laden
Zum Laden verwenden Sie bitte die Kindergarten-DB, sofern mehrere Datenbanken angezeigt werden.
Laden Sie folgende Tabellen:
* adresse
* arbeitszeit
* arbeitszeitzuordnung
* betreuerin
* elternteil
* familienverhältnis
* gruppe
* kind
* raum

## Aufgabe 3: Datenmodell anzeigen
Sie sollten nun im Bildschirm "Tabellentools" die Daten der ersten Tabelle sehen können. 
 ![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/5b266e66-e6de-4060-a076-b522604e62f3)

Wechseln Sie nun auf die "Modellansicht"
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/824d0272-21c5-43c9-93e4-407c73569924)

PowerBI zeigt Ihnen nun das Datemodell zu den geladenen Tabellen an. 
  ![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/2144f6b0-0f05-461b-ba02-3ae50405c555)

Falls notwendig, können Sie hier mittels Drag&Drop Beziehungen zwischen den Tabellen anpassen. PowerBI kann Fremdschlüsselbeziehungen in Datenbanken auswerten und ist auch in der Lage aus Spaltenüberschriftn in Excel Fremdschlüsselbeziehungen zu generieren.

## Aufgabe 4: Daten transformieren
Klicken Sie nun auf "Daten transformieren" im Bereich "Abfragen".   
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/27e81c63-ca46-43be-89a6-59077d78f18f)

Aus Gründen der Lesbarkeit möchten Sie in der Tabelle **"elternteil"** die Flag-Spalten (IstHauptansprechpartner, Whatsappzugehörigkeit und IstBerufstaetig) in Boolean umformen. Klicken Sie dazu mit einem Rechtsklick auf die Spaltenüberschriften und wählen Sie aus "Typ ändern". 

Benennen Sie die Spalten um:
* IstHauptansprechpartner --> Hauptansprechpartner?
* IstBeruftstaetig --> berufstätig?
* Whatsapp zugehörigkeit --> InWhatsAppGruppe?

Speichern Sie nun die Änderungen. Sie werden eine Fehlermeldung erhalten. 
Brechen Sie die Verarbeitung ab und fahren Sie mit der nächsten Aufgabe fort.

## Aufgabe 5: Daten bereinigen
Prüfen Sie die Einträge in der Tabelle "elternteil" und bereinigen Sie die Daten durch Ersetzen der Werte. Sie legen durch diesen Schritt eine Bereinigungsfunktion an :-)

Prüfen Sie auch alle anderen Tabellen auf Fehler und löschen Sie überflüssige Spalten (Zusatzinfo in Adresse).


## Aufgabe 6: Visualisierung

Eine Darstellung der Widgets (Visuals) für PowerBI finden Sie [hier](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)  

Erstellen Sie zusammen mit Ihrem Team eine Visualisierung, die folgendes zeigt:
1) Anzahl der Kinder pro Gruppe
2) Anzahl der Betreuerinnen pro Gruppe

Beispiel:  
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/d76868de-dad0-49df-9ff6-295f01ef9050)

Achtung: Die Darstellung der Kinder pro Gruppe ist nicht korrekt. 
Gehen Sie ins Datenmodell zurück und aktivieren Sie die Beziehung zwischen Kind und Gruppe:  
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/e86c31bb-92da-4e1b-a99e-0f9cfbaf195d)


# Wie geht es weiter?
In der Übung haben Sie einen kleinen Teil von PowerBI kennen gelernt und ein Dashboard entworfen. 
In einem Unternehmen wäre es nun wichtig, das Dashboard zu publizieren (publish).  
Hierzu könnten Sie das Dashboard im Cloud Service von PowerBI hochladen und anderen Team-Mitgliedern zur Verfügung stellen. 
