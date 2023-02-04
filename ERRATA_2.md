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


## Abschnitt 7.2, S. 159 zweiter Absatz

** Fehler:**

Es hat sich ein 'Sie' zuviel eingeschlichen. Es muss heißen:

Sie können eine Modul-Dokumentation auch offline lesen mit dem Befehl:


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
