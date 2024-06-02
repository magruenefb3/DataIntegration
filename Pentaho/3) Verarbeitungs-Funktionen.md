# Verarbeitungslogik in PDI

## Merging - Datenquelle miteinander verbinden
Merging bedeutet, dass Daten kombiniert werden. Bei einem Merge wird inhaltlich eine Vereinigungsmenge aus mehreren Datenquellen gebildet. 

### Sorted Merge
Vor eineme Sorted Merge müssen die einzelnen Datenstreams nach einem Attribut sortiert werden. I.d.R. ist das der Key. 

Das Vorgehen ist wie folgt:
1) Daten laden und beim Laden **deduplizieren** (anhand des Keys).
2) Daten sortieren mit Transform --> "Sort rows"
3) Daten mit Joins --> "Sorted merge" zusammenführen.

![image](https://github.com/magruenefb3/DataIntegration/assets/97667586/b9381cea-557d-46e9-b278-b8d66a5ad63f)
