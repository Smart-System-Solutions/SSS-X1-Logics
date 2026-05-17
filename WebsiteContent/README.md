# Website-Content

Dieser Ordner enthält den Index für Website-Inhalte, die direkt aus dem Git-Repository gelesen werden können.

- `index.de.json` listet alle Bausteine und deren Content-Dateien.
- Jeder produktive Baustein besitzt eine eigene Datei `WebsiteContent.de.json` im jeweiligen Projektordner.
- Die Inhalte sind in feste Abschnitte gegliedert: Kurzbeschreibung, Besonderheiten, detaillierte Beschreibung, Eingänge, Ausgänge, Beispiele, FAQ und Changelog.
- `Build-WebsiteContent.ps1` erzeugt die Dateien reproduzierbar aus Manifest, Code-Metadaten und optional vorhandenen Website-Seiten.

Die Website sollte bevorzugt `index.de.json` lesen und anschließend die referenzierten Baustein-Dateien laden.

Beim Release-Build mit Distribution kopiert `00_Dokumente\Signieren\BuildLogicPackages.ps1` die Inhalte zusätzlich nach `SSS-X1-Logics`:

- `WebsiteContent/index.de.json`
- `<Baustein>/WebsiteContent.de.json`

Dadurch kann die Website später direkt aus dem GitHub-Repository `SSS-X1-Logics` lesen, ohne die signierten ZIP-Dateien entpacken zu müssen.
