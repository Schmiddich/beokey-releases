# Beokey-Releases

Dieses öffentliche Repository enthält ausschließlich veröffentlichte Installationsdateien und die Update-Informationen für [Beokey](https://github.com/Schmiddich/voicely-klon).

Der Quellcode von Beokey bleibt privat und liegt nicht in diesem Repository. Es gibt hier bewusst weder Quellcode noch Build-Zwischenstände.

## Struktur

- Pro Version existiert ein GitHub Release mit dem Tag `v<Version>` (beispielsweise `v0.1.0`). Das Installer-Asset heißt `BeokeySetup-<FileVersion>.exe`.
- Die App liest für Update-Prüfungen ausschließlich diese stabile URL: `https://raw.githubusercontent.com/Schmiddich/beokey-releases/main/latest.json`.
- `latest.json` enthält die aktuelle Version, den direkten HTTPS-Download, SHA-256, Dateigröße, Hinweise und die Mindestversion. Die App prüft SHA-256 und Dateigröße vor dem Start des Installers.

Der Release-Ablauf im privaten Quellcode-Repository aktualisiert `latest.json` erst, nachdem das passende GitHub Release samt Installer veröffentlicht wurde.
