# AWB Köln – Abfuhrtermine (GitHub Pages Widget)

Dieses Repo enthält:
- `awb_static.html` – Widget, das **awb.ics** (gleiche Origin) lädt und anzeigt
- `awb.ics` – wird **täglich** per GitHub Action aktualisiert
- `.github/workflows/fetch-awb.yml` – holt den ICS-Feed von AWB Köln und committet Änderungen

## Nutzung
1. Dieses Repo als **GitHub Pages** veröffentlichen (Branch: `main`, Ordner: `/root`).
2. Action läuft täglich und schreibt **awb.ics** in den Repo-Root.
3. Binde die Seite so ein:
   ```html
   <iframe src="https://DEINNAME.github.io/DEINREPO/awb_static.html"
           style="width:100%;border:none;height:360px;"></iframe>
   ```
4. Keine CORS-Probleme, da `awb_static.html` und `awb.ics` **vom gleichen Origin** geladen werden.

## Manuell testen
- Führe die Action einmal mit **Run workflow** aus (Tab „Actions“).