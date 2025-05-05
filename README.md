## Ülesanne 1: Failide õiguste kontroll

Kirjutage funktsioon nimega `permissions_check.py`, mis:

- Kontrollib, kas teatud kataloogis (nt `/var/www/`) luuakse või muudetakse faile õigustega **777** (loe-, kirjuta- ja käivitaõigus kõigile).
- Kui leitakse fail õigustega **777**, siis:
    - Faili õigusi muudetakse **`*rw-rw-r--*`** vastu,
    - Sündmusest kirjutatakse log-faili `permission-control.log` kasutaja kodukatalogis, kirjeldus sisaldab kustutamise aega formaadis YYYY-MM-DD HH:MM ja failinimi.

---

## Ülesanne 2: Failide kogumahu arvutamine

Kirjutage funktsioon nimega `pdf_calulation.py`, mis arvutab .pdf-failide kogumaht sisselogitud kasutaja kodukataligis ja selle alamkataloogides. Kasuta keskkonnamuutujaid operatsioonisüsteemi tuvastamiseks.

---

## Ülesanne 3: Failide sorteerimine vanuse järgi

Kirjutage skript `file_sorting.py`, mis:

- Sorteerib failid kasutaja kodukataloogis nende **muutmiskuupäeva** alusel.
- Teisaldab kõik failid kodukatalogist ja alamkataloogidest, mis on **vanemad kui 7 päeva**, kausta "archive", mis asub kasutaja kodukatalogis.

---

## Ülesanne 4: Kataloogistruktuuri teisendamine JSON-formaati

Kirjutage Pythoniga skript, mis teisendab kasutaja kodukataloogi struktuuri järgmisse JSON-formaati ja salvestab faili `hometree.json`:
```
{
  "name": ".",
  "path": ".",
  "mask": "775",
  "owner": "username",
  "type": "directory",
  "children": [
    {
      "name": "file_age.py",
      "path": "./file_age.py",
      "mask": "664",
      "owner": "username",
      "type": "file"
    },
    {
      "name": "mv_old_files.py",
      "path": "./mv_old_files.py",
      "mask": "664",
      "owner": "username",
      "type": "file"
    },
    {
      "name": "jsonparse.py",
      "path": "./jsonparse.py",
      "mask": "664",
      "owner": "username",
      "type": "file"
    },
    {
      "name": "subfolder",
      "path": "./subfolder",
      "mask": "775",
      "owner": "username",
      "type": "directory",
      "children": [
        {
          "name": "temp.txt",
          "path": "./subfolder/temp.txt",
          "mask": "664",
          "owner": "username",
          "type": "file"
        }
      ]
    }
  ]
}
```


