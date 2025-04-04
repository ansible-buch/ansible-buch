# Errata zur dritten Auflage

## Abschnitt 5.9.1, S. 95, erster Textabsatz

**Fehler:**

Es ist nicht der `create`-Parameter, sonder der `creates`-Parameter.
Der letzte Satz muss also lauten:

Das machen wir uns auch sogleich mit dem
`creates`-Parameter zunutze, um für Idempotenz zu sorgen:
[...]


## Abschnitt 6.9.1, S. 148, Listing 6.47 unten

**Problem**: Die Listingunterschrift ist nicht genau genug. Sie sollte lauten:

`flatten-list-loop.yml`: Beispiel einer `with_items`-Schleife über eine
verschachtelte Liste
