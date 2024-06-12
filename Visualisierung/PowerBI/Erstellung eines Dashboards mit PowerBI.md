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

Sie sollten nun im Bildschirm "Tabellentools" die Daten der ersten Tabelle sehen können. 
 ![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/5b266e66-e6de-4060-a076-b522604e62f3)



# Wie geht es weiter?
In der Übung haben Sie einen kleinen Teil von PowerBI kennen gelernt und ein Dashboard entworfen. 
In einem Unternehmen wäre es nun wichtig, das Dashboard zu publizieren (publish).  
Hierzu könnten Sie das Dashboard im Cloud Service von PowerBI hochladen und anderen Team-Mitgliedern zur Verfügung stellen. 
