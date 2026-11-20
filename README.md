# DIVERSION Updates 🐒🍌

Öffentliche macOS-Installationsdateien für **DIVERSION**, einen VST3-Synthesizer für Ableton Live.

**Der DIVERSION-Quellcode ist privat.** Dieses Repository enthält nur Informationen und fertige Installationsdateien. Der Quellcode steht derzeit nicht unter einer Open-Source-Lizenz.

## Erstinstallation

1. Lade auf der [Releases-Seite](https://github.com/captnhanky/DIVERSION-Updates/releases) die neueste `DIVERSION-Installer.dmg` herunter.
2. Öffne die DMG und beende Ableton Live vollständig.
3. Starte **DIVERSION installieren.command**.
4. Öffne Ableton Live und gegebenenfalls den VST3-Scan.

## Updates direkt im Plugin (ab v0.9.0)

- **UPDATE** prüft diese öffentlichen GitHub Releases.
- Bei einer neueren Version wird **GET vX.Y.Z** angezeigt.
- Erneuter Klick startet den Download über den lokalen macOS-Update-Helfer.
- Nach geprüftem SHA-256-Hash erscheint **QUIT LIVE**. Beende Ableton Live: Der Helfer installiert die VST3 selbstständig und legt bei einem Fehler die vorige Version wieder zurück.
- Neustart von Ableton Live lädt die neue Version.

Der lokale Update-Helfer wird zusammen mit DIVERSION installiert; **GitHub-Releases führen keine heruntergeladenen Skripte aus**. Das Update wird ausschließlich installiert, wenn GitHub einen SHA-256-Digest für das DMG bereitstellt. Die genaue Version ist im Plugin oben sichtbar.

**Die Funktion benötigt einen veröffentlichten DMG-Release.** Ein leeres Releases-Verzeichnis liefert noch keine Updates.

Die VST3 ist zurzeit **nicht Apple-signiert oder notarisiert**. Auf macOS kann deshalb bei der ersten Installation eine Sicherheitsfreigabe erforderlich sein.

## Für die Veröffentlichung

Das private Build-Repository kann erfolgreiche DMGs automatisch als Release in dieses öffentliche Repository hochladen. Dafür ist im privaten Repo das GitHub Actions Secret `DIVERSION_UPDATES_TOKEN` nötig: ein Fine-grained Personal Access Token mit **Contents: Read and write**, ausschließlich für `captnhanky/DIVERSION-Updates`. Der Token darf niemals im Plugin oder in einem Commit gespeichert werden.

Release-Tags müssen zum Plugin passen (beispielsweise `v0.9.0`) und ein Asset namens `DIVERSION-Installer.dmg` enthalten. Bestehende Versionen werden nicht stillschweigend ersetzt.
