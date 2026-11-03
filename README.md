# Ideen-Priorisierer

Prototyp für die AI Coding Challenge: Ideen erfassen, von einer KI bewerten lassen und nach ihrem Nutzen pro Jahr in Euro sortieren.

**Live-Demo:** https://vladislav7-tech.github.io/Ideen-Priorisierung/

## So funktioniert es

1. Pro Idee angeben: wie viele Personen betroffen sind, was eine Arbeitsstunde kostet und wie viele Stunden pro Woche eine Person heute mit dieser Aufgabe verbringt.
2. API-Key eintragen (Claude oder OpenAI, wird automatisch erkannt) und „Ideen bewerten“ klicken.
3. Die KI schätzt pro Idee: wie viel Prozent der heutigen Zeit wegfallen (Unsicherheit bereits eingepreist), den Umsetzungsaufwand und laufende Kosten – mit kurzer Begründung.
4. Ergebnis: Ranking nach Nutzen pro Jahr. Ein Klick auf eine Idee zeigt Begründung, Risiko und die Werte, die man selbst anpassen kann.

## Berechnung

```
Zeitersparnis = Personen × Std./Woche heute × Ersparnis % × €/Stunde × 44 Wochen
Nutzen / Jahr = Zeitersparnis − Umsetzungsaufwand (Stunden × €/Stunde) − laufende Kosten
```

Die KI liefert nur Schätzwerte und Begründung. Das Ranking ist eine transparente Formel und damit nachvollziehbar.

## Datenschutz

Alle Daten bleiben im Browser. An die KI werden nur die Ideen und ihre Zahlen gesendet. Der API-Key ist nicht im Code enthalten und wird nur lokal gespeichert.
