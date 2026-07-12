# BaudokuXtrem · SKR

Baudokumentation für Sachverständige.
Bausachverständigenbüro Stefan Klaus Ritter, Schorndorf.

## Aufbau

Der App-Kern liegt **ausschließlich verschlüsselt** in diesem Repository
(`baudokuxtrem.enc`, AES-GCM-256, PBKDF2-HMAC-SHA256 mit 310.000 Iterationen).

`index.html` ist ein reiner **Loader**: wenige Kilobyte, ohne App-Inhalt.
Er holt den verschlüsselten Container, entschlüsselt ihn **lokal im Browser**
und startet die App. Ohne gültiges Master-Passwort passiert nichts.

## Was hier bewusst NICHT liegt

- kein Klartext der App
- keine Mandantendaten, keine Akten
- keine Zugangsdaten, keine API-Schlüssel
- die Lizenz-Datenbank enthält ausschließlich SHA-256-Hashes, keine Klarnamen
