# Ideen-Priorisierer

Prototyp für die AI Coding Challenge: Ein Team erfasst Ideen, eine KI schätzt Zeitersparnis und Kosten, und die App sortiert die Ideen nach ihrem Nutzen pro Jahr in Euro.

**Live-Demo:** https://vladislav7-tech.github.io/Ideen-Priorisierung/

## So funktioniert es

1. Team beschreiben: Stundensatz, Anzahl Personen, Arbeitswochen, kurze Beschreibung der Arbeit.
2. Ideen erfassen (oder Beispiele laden).
3. API-Key eintragen (Claude oder OpenAI, wird automatisch erkannt) und „Ideen bewerten“ klicken.
4. Ergebnis: Ranking nach Nutzen pro Jahr. Ein Klick auf eine Idee zeigt Begründung, Risiko und die Werte, die man selbst anpassen kann.

## Berechnung

```
Nutzen pro Jahr = Personen × Ersparnis h/Woche × Stundensatz × Wochen × Konfidenz
                  − Umsetzungsaufwand (h × Stundensatz)
                  − laufende Kosten pro Jahr
```

Die KI liefert nur die Schätzwerte und die Begründung. Das Ranking selbst ist eine transparente Formel und damit nachvollziehbar.

## Datenschutz

Alle Daten bleiben im Browser. An die KI werden nur Ideentexte und Teambeschreibung gesendet. Der API-Key ist nicht im Code enthalten und wird nur lokal gespeichert.
