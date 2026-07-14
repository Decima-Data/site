# Decima Landing Page

Statische Ein-Seiten-Website für decima.lu. Kein Build-Schritt, keine Abhängigkeiten — nur `index.html` + `CNAME`.

## Live schalten (GitHub Pages, kostenlos)

Voraussetzung: GitHub-Account mit `lou@decima.lu` + Organisation `decima-data` existieren.

1. **Repo anlegen:** In der Org `decima-data` ein neues öffentliches Repo `site` erstellen.
2. **Dateien hochladen:** `index.html`, `CNAME` und diese README ins Repo pushen (oder im Browser per "Add file → Upload files").
3. **Pages aktivieren:** Repo → Settings → Pages → Source: "Deploy from a branch" → Branch `main`, Ordner `/ (root)` → Save.
4. **Custom Domain:** Im selben Pages-Menü unter "Custom domain" `decima.lu` eintragen (die CNAME-Datei liegt schon im Repo). Häkchen bei "Enforce HTTPS" setzen, sobald verfügbar (kann bis zu 24h dauern).
5. **DNS bei EuroDNS setzen:** Dashboard → decima.lu → DNS-Einträge:
   - Vier **A-Records** für die nackte Domain (`@`):
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Ein **CNAME-Record** für `www` → `decima-data.github.io`
   - Achtung: Die Mail-Einträge (MX, SPF/TXT) NICHT anfassen — die gehören zum Postfach.
6. **Warten & prüfen:** DNS braucht Minuten bis Stunden. Danach ist die Seite unter https://decima.lu erreichbar.

## Später ändern

`index.html` bearbeiten → pushen → Seite aktualisiert sich automatisch in ~1 Minute.

Offene Platzhalter:
- [ ] Hugging-Face-Link im "Datasets"-Abschnitt eintragen, sobald das Chamber-Korpus online ist
- [ ] Optional: "Founded by <Name>" im Contact-Abschnitt ergänzen
