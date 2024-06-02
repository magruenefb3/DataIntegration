# Data Cleansing

Hinweis: wenn in den folgenden Funktionen ein "Out (Stream) Field" gesetzt wird, wird eine neue Spalte erstellt. 

## Value Mapper - Mapping von Source in Target Datenwerte
Wenn in Daten falsche Werte erfast sind, können diese z.B. durch einen Lookup in einer Mapping-Tabelle korrigiert werden. 
So kann es sein, dass für ein Land das Kürzel "D" oder "BRD" erfasst wurde, obwohl der korrekte Wert auf "Deutschland" gesetzt sein sollte.

Die Verarbeitung kann durch `Transform --> Value mapper` definiert werden.  
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/f2e2536b-d2a6-4a4e-8165-8d736d79168a)

Problematisch dabei ist, das Value Mapper nur bei einer geringen Anzahl von Werten sinnvoll eingesetzt werden kann.

## String-Substitution
Mit `Transform --> Replace in String` können z.B. mittels RegEx oder Buchstabenersetzung Korrekturen an Daten vorgenommen werden.

## Fuzzy Match mit Lookup-Tabellenwerten
![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/3c7526ae-b112-4110-8e9d-9e53790afc15)

