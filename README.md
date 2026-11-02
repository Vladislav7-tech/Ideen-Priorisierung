# Intelligenter Ideen-Priorisierer

Prototyp für die AI Coding Challenge: Ein Team erfasst Ideen, eine KI schätzt Zeit- und Kosteneffekte, und die App priorisiert die Ideen nach ihrem wirtschaftlichen Nutzen.

**Live-Demo:** https://vladislav7-tech.github.io/Ideen-Priorisierung/

## Funktionen

- Ideen erfassen (oder 10 Beispielideen laden)
- Team-Kontext angeben: Stundensatz, Teamgröße, Arbeitswochen, Beschreibung
- Bewertung durch **Claude (Anthropic API)** oder **regelbasiert** als Fallback ohne KI
- Berechnung in Euro: Nutzen pro Jahr, Einmalaufwand, Netto im 1. Jahr, Amortisationszeit
- Ranking mit Kategorien: Quick Win / Lohnend / Prüfen
- Begründung, Annahmen, Risiken und nicht-monetärer Nutzen pro Idee
- Werte manuell anpassen („Die KI schlägt vor, der Mensch entscheidet“)
- Diagramm Aufwand vs. Nutzen
- Export als CSV und Markdown

## Berechnung

```
Nutzen/Jahr   = betroffene Personen × Ersparnis h/Woche × Stundensatz × Arbeitswochen × Konfidenz
Einmalaufwand = Umsetzungsstunden × Stundensatz
Netto 1. Jahr = Nutzen/Jahr − Einmalaufwand − laufende Kosten
Amortisation  = Einmalaufwand ÷ monatlicher Netto-Nutzen
```

Die KI liefert nur die Schätzwerte. Die Priorisierung selbst ist eine transparente Formel und damit nachvollziehbar und reproduzierbar.

## Nutzung

1. `index.html` im Browser öffnen (oder Live-Demo).
2. Für den KI-Modus einen eigenen Anthropic API-Key eintragen. Ohne Key wird automatisch regelbasiert bewertet.

## Datenschutz

- Alle Daten bleiben im Browser (localStorage), es gibt keinen eigenen Server.
- Im KI-Modus werden nur Ideentexte und Team-Kontext an die Anthropic-API gesendet.
- Der API-Key ist nicht im Code enthalten und wird nur lokal im Browser gespeichert.
