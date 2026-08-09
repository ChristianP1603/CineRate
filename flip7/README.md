# Flip 7 – Punktezähler

Ein Punktezähler für das Kartenspiel **Flip 7** als reine Web-App: eine einzige
`index.html` ohne Build-Schritt, ohne Abhängigkeiten, ohne Server. Einfach im
Browser öffnen – funktioniert auch offline.

## Features

- **Spielerverwaltung** – 2 bis 18 Spieler, frei benennbar, feste Farbzuordnung
- **Kartenweise Eingabe** – Zahlenkarten 0–12 antippen statt im Kopf rechnen
- **Modifikatoren** – `+2 +4 +6 +8 +10` und `×2` mit korrekter Rechenreihenfolge
- **Bust** – ein Tipp setzt die Runde auf 0, Karten bleiben zur Kontrolle sichtbar
- **Flip-7-Bonus** – wird bei sieben verschiedenen Zahlen automatisch erkannt (+15)
- **Live-Formel** – zeigt jederzeit, wie sich die Rundenpunkte zusammensetzen
- **Rundenverlauf** – Tabelle aller Runden; jede Zelle ist antippbar und nachträglich korrigierbar
- **Statistik** – Schnitt, beste Runde, Busts und Flip 7s pro Spieler
- **Zielpunktzahl** – frei einstellbar, Standard 200 wie im Original
- **Sieger-Screen** mit Endstand, Konfetti und Revanche-Button
- **Automatisches Speichern** – der Spielstand überlebt Reload und Appwechsel
- **Undo** – letzte Runde per Menü zurücknehmen
- **Regelreferenz** direkt in der App
- Mobil-first, große Touch-Flächen, Tastaturbedienung am Desktop

## Nutzung

`flip7/index.html` im Browser öffnen. Zum Hosten reicht jeder statische
Webspace – z. B. GitHub Pages: in den Repo-Einstellungen unter *Pages* den
Branch wählen, danach liegt die App unter `…/flip7/`.

### Tastatur (Desktop, im Eingabedialog)

| Taste | Wirkung |
|---|---|
| `0`–`9` | Zahlenkarte umschalten |
| `1` dann `0`/`1`/`2` | Karte 10 / 11 / 12 |
| `B` | Bust umschalten |
| `Enter` | Weiter / Runde abschließen |
| `Esc` | Dialog schließen |

## Wertung

```
Bust                → 0 Punkte
sonst               → (Summe der Zahlenkarten × 2 falls ×2)
                       + Plus-Modifikatoren
                       + 15 bei sieben verschiedenen Zahlen
```

Die `×2`-Karte verdoppelt ausschließlich die Summe der Zahlenkarten – die
Plus-Karten und der Flip-7-Bonus kommen erst danach dazu. Bei einem Bust
verfallen auch die Modifikatoren.

`Freeze` und `Flip Three` steuern nur den Spielablauf und haben keinen
Einfluss auf die Wertung; sie werden deshalb nicht erfasst.
