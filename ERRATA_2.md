# Errata zur zweiten Auflage

## Abschnitt 4.2, S. 66, Listing 4.2

**Fehler/Problem:**

Die gezeigte `.vimrc` führt zu einem gewöhnungsbedürftigen Einrückverhalten
bei YAML-Dateien:
Vim rückt in einer neuen Zeile erst einmal unnötig ein, um dann ggf. 
während des Tippens eines Doppelpunktes wieder "zurückzurücken".

**Abhilfe:** 

Wenn Sie sich daran stören, streichen Sie in der ersten Zeile das Wort
`indent`. Also nur `filetype on` (oder auch `filetype plugin on`).


## Abschnitt 7.1.2, S. 158 unten

**Fehler:**

Der Name des Listings lautet natürlich `meta/main.yml`.


## Abschnitt 7.2, S. 159 zweiter Absatz

**Fehler:**

Es hat sich ein 'Sie' zuviel eingeschlichen. Es muss heißen:

Sie können eine Modul-Dokumentation auch offline lesen mit dem Befehl:


## Abschnitt 7.7, S. 170 unten

**Fehler/Problem:**

Als Beispiel für den Einsatz des `uri`-Moduls wird die Abfrage einer REST-API
für Chuck Norris-Witze gezeigt. Leider funktioniert diese (Stand Februar 2023)
nicht mehr wie gewünscht. Chuck Norris ist aber nicht verloren;
er steht weiterhin z.B. hier zur Verfügung:

```
- name: Einen Chuck-Norris-Witz besorgen
  uri:
    url: https://api.chucknorris.io/jokes/random
    return_content: yes
  register: this

- debug: var=this.json.value
```

## Abschnitt 13.1.1, S. 295 oben

**Fehler/Problem:**

Es gibt offenbar neuerdings Probleme mit dem Debian-11-Paket `python3-hcloud`.
Hetzner scheint irgendetwas an der API geändert zu haben, sodass das 
in der Folge gezeigte Playbook bzw. die dynamischen Inventory-Zugriffe
nicht mehr fehlerfrei funktionieren. (Stand: Mai 2022)

**Abhilfe:** 

Sollten Sie davon betroffen sein, verwenden Sie stattdessen das aktuelle
Python-Modul:

```
sudo apt purge python3-hcloud
sudo pip3 install hcloud
```

## Abschnitt 15.4, S. 329 mitte

**Fehler/Problem:**

Das PowerShell-Skript `ConfigureRemotingForAnsible.ps1` ist auf GitHub
"umgezogen". Die neue URL lautet:

https://github.com/ansible/ansible-documentation/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
