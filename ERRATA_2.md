# Errata zur zweiten Auflage

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
