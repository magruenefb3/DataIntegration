# Verarbeitungslogik in PDI

## Merging - Datenquellen miteinander verbinden
Merging bedeutet, dass Daten kombiniert werden.   
Bei einem Merge wird inhaltlich eine Vereinigungsmenge aus mehreren Datenquellen gebildet. 

### Sorted Merge
Vor eineme Sorted Merge müssen die einzelnen Datenstreams nach einem Attribut sortiert werden. I.d.R. ist das der Key. 

Das Vorgehen ist wie folgt:
1) Daten laden und beim Laden **deduplizieren** (anhand des Keys).
2) Gegebenenfallss mit  `Transform --> Select values` die Reihenfolge der Spalten einzelner Inputs anpassen, damit alle Inputs dasselbe Datenschema haben. 
Auch Daten(typ)konvertierungen können mit dieser Funktion implementiert werden.
3) Daten sortieren mit `Transform --> Sort rows`
4) Daten mit `Joins --> Sorted merge` zusammenführen.
5) Zum Schluss wird das Ergebnis mit `Transform --> Unique rows` erneut dedupliziert.

![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/2220b2ef-f772-4774-89c5-dcf185396123)

### Hinweise zum Sortieren von Daten(spalten)
Mit  `Transform --> Select values` können Datenspalten ausgewählt oder in der Reihenfolge geändert werden. 
Auch Daten(typ)konvertierungen können mit dieser Funktion implementiert werden.
