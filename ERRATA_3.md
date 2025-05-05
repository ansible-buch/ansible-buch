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


## Abschnitt 12.3, S. 305, Listing 12.3

**Problem**: Die Einrückung der ersten Zeile ist verloren gegangen.
Das Keywort `vars` sollte erst nach 6 Spaces kommen:

```yaml
      vars:
        # ...
        animals:
          - name: Lassie
            age:  7
          - name: Kitty
            age:  9
```
