# Frame Time Overlay / Anzeige der Uhrzeit

Dieses kleine HTML/JS-Script zeigt die aktuelle Uhrzeit **bis auf Millisekunden genau** direkt im Browser an.  
Es ist gedacht für technische Tests, um die **Latenz von Screen zu Screen** oder innerhalb komplexer **Streaming-Pipelines** zu messen.

---

## Zweck

- Überlagert die Uhrzeit auf einem Bildschirm
- Per Screenshot oder Snapshot lassen sich Zeitdifferenzen zwischen verschiedenen Screens vergleichen
- Hilfreich bei Debugging und Optimierung von Streaming-Setups mit mehreren Knoten

---

## Funktionsweise

- Die Anzeige basiert auf einer Kombination aus `Date.now()` und `performance.now()`  
  → sorgt für kontinuierlich präzise Darstellung
- Aktualisierung erfolgt mit `requestAnimationFrame()` für flüssige Wiedergabe
- Format: `HH:MM:SS.mmm` (Stunden, Minuten, Sekunden, Millisekunden)
- Minimalistisches Design für klare Lesbarkeit auch bei Aufnahmen oder Snapshots

---

## Nutzung

1. Datei `uhrzeit.html` im Browser öffnen  
2. Uhrzeit erscheint sofort mittig auf dem Bildschirm  
3. Mit Kamera, Screenshot oder Framegrabber aufnehmen → Zeitdifferenzen zwischen Screens analysieren

---

## Einsatz in OBS Studio

Diese HTML-Datei kann direkt als **Browser-Quelle** in OBS Studio eingebunden werden.  
So erscheint die präzise Uhrzeit im Livestream oder in der Aufnahme und kann dort zur **Messung von Latenzen** genutzt werden.

---

## Beispiel-Anwendung

- Latenz-Test zwischen zwei Monitoren
- Messung von Verzögerungen in Streaming-Ketten (z. B. OBS → MediaMTX → Restreamer → Player)
- Dokumentation von End-to-End-Verzögerungen über mehrere Systeme hinweg

---

## Hinweis

Dieses Tool ersetzt keine präzise Messtechnik, liefert aber eine einfache visuelle Möglichkeit, **End-to-End-Latenzen** mit minimalem Aufwand zu überprüfen.

