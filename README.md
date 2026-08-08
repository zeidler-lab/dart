# ZDR

Dart-Zähler als Web-App: X01 (301/501/701), Cricket, Around the Clock, Shanghai, Count Up und Halve It.
Läuft im Browser, lässt sich auf dem Handy als App installieren und funktioniert danach auch ohne Netz.

## Funktionen

**X01**
- Drei Eingabearten: einzelne Felder (Faktor + Zahl), drei Zahlen nacheinander, oder Aufnahme-Summe
- Double Out an/aus, bei Feldeingabe wird das Doppel echt geprüft
- Finish-Weg für jeden Rest bis 170, passend zu den verbleibenden Darts, mit Anzeige auf dem Board
- Bust-Erkennung, Legs und Sätze, wechselnder Anwurf
- Statistik: 3-Dart-Average, Darts, 180er, höchste Aufnahme, bestes Finish, bestes Leg, Doppelquote

**Cricket** – normal und Cut Throat, klassische Tafel mit Marks, Punkten und MPR.

**Around the Clock** – 1 bis 20 und Bull der Reihe nach, Platzierung nach Darts.

**Shanghai** – Runde 1 auf die 1, Runde 2 auf die 2 und so weiter. Einfach, doppelt und dreifach derselben Zahl in einer Aufnahme gewinnt sofort.

**Count Up** – Punktesammeln über feste Runden, höchste Summe gewinnt.

**Halve It** – feste Ziele je Runde (20, 19, 18, Doppel, 17, Dreifach, genau 41, Bull). Keine Zahl getroffen heißt Punktestand halbiert. Start bei 40.

**Allgemein**
- „Dart zurück" nimmt einzelne Würfe zurück, auch über den Spielerwechsel hinaus
- Gespeicherte Spielernamen, Verlauf der letzten 30 Spiele, gemerkte Einstellungen
- Animationen bei 100+, 140+, 180, Checkouts, Nine Darter und Bust

## Auf GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, z. B. `zdr`, Sichtbarkeit **Public**.
2. Im leeren Repo auf **uploading an existing file** klicken und alle Dateien aus diesem Ordner hochladen:
   `index.html`, `manifest.json`, `sw.js`, `README.md`, `.nojekyll`,
   `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png`, `favicon.png`
3. **Commit changes** klicken.
4. Im Repo auf **Settings → Pages** gehen.
5. Unter *Build and deployment* bei *Source* **Deploy from a branch** wählen,
   Branch **main**, Ordner **/ (root)**, dann **Save**.
6. Nach ein bis zwei Minuten ist die App erreichbar unter
   `https://DEIN-BENUTZERNAME.github.io/zdr/`

Wichtig: alle Dateien müssen im Hauptverzeichnis des Repos liegen, nicht in einem Unterordner.
Falls du sie doch in einen Ordner legst, ändert sich nur die Adresse entsprechend.

## Auf dem Handy installieren

**iPhone / iPad:** Adresse in **Safari** öffnen (nicht Chrome) → Teilen-Symbol → *Zum Home-Bildschirm*.

**Android:** Adresse in **Chrome** öffnen → Menü (drei Punkte) → *App installieren*.

**Desktop:** In Chrome oder Edge erscheint rechts in der Adressleiste ein Installieren-Symbol.

## Daten

Spieler, Verlauf und Einstellungen liegen im Speicher des Browsers auf dem jeweiligen Gerät.
Kein Server, kein Konto, keine Übertragung. Andere Geräte haben eigene Daten,
und wer die Browserdaten löscht, löscht auch den Verlauf.

## Updates einspielen

Geänderte Dateien im Repo ersetzen. Damit installierte Geräte die neue Version sicher ziehen,
in `sw.js` die Zeile `const CACHE = "zdr-v2";` hochzählen, z. B. auf `zdr-v3`.
