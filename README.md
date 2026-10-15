# Firmenordner-Vorlage

Vorlage für ein gemeinsames KI-Betriebssystem im Team: ein Firmenordner, den alle mit Claude nutzen, jeder aus seinem eigenen Arbeitsordner heraus. Das Firmenwissen ändert nur, wer dafür zuständig ist, alle anderen schlagen Änderungen vor.

Die Vorlage gehört zum Kurs „KI-Betriebssystem“ in der [Community KI-Automatisierung](https://www.skool.com/ki-automatisierung), Abschnitt „AI-OS im Unternehmen einrichten“. Dort steht, warum der Firmenordner so aufgebaut ist und wie ihr ihn Schritt für Schritt einführt.

## Was drin ist

```
grundregeln.md        wie die Arbeit mit dem Firmenordner funktioniert, bei jeder Firma gleich
CLAUDE.md             was nur für eure Firma gilt, bindet die Grundregeln ein
wissen/               Firmenwissen: Leistungen, Preise, Schreibstil, Abläufe
.claude/skills/       Skills, die das ganze Team nutzt
arbeit/               laufende Arbeit: Angebote, Kundenprojekte, Notizen
vorschläge/           Änderungswünsche ans Firmenwissen
einrichtung/          Willkommensnachricht mit Startprompt für neue Kollegen
```

Die `grundregeln.md` passt ihr nicht an. Was bei euch anders laufen soll, schreibt ihr in die `CLAUDE.md` unter „Bei uns anders“. Dann könnt ihr neue Versionen der Grundregeln einfach übernehmen.

## Einrichten

Mit GitHub: Leg für deine Firma eine Organisation auf GitHub an und sag Claude in deinem eigenen Arbeitsordner:

> Erstell aus der Vorlage `Julian-Ivanov/firmenordner-vorlage` ein privates Repo in meiner GitHub-Organisation [Name] und hol es als Unterordner `firma/` in meinen Ordner.

Mit SharePoint, OneDrive oder Google Drive: Leg im Sync-Ordner einen leeren Ordner an und sag Claude:

> Lade die Vorlage von https://github.com/Julian-Ivanov/firmenordner-vorlage/archive/refs/heads/main.zip herunter und entpack den Inhalt nach [Pfad zum Ordner].

Danach füllt Claude mit dir die `CLAUDE.md` und `wissen/` aus. Die genauen Prompts stehen im Kurs.

## Ein Vorschlag

Wer das Firmenwissen ändern will, sagt Claude „schlag das dem Team vor“. Claude legt dann zum Beispiel `vorschläge/2026-10-15-anna-tagessatz.md` an:

```
Betrifft: wissen/leistungen-und-preise.md
Änderung: Tagessatz von 1.200 Euro auf 1.400 Euro
Grund: Seit 1. Oktober gilt der neue Satz, so mit dem Chef besprochen.
Von: Anna
```

Die zuständige Person sagt „geh die Vorschläge durch“ und entscheidet pro Vorschlag.

## Neue Grundregeln übernehmen

Die Versionsnummer steht oben in der `grundregeln.md`. Ob es eine neuere gibt, prüft Claude für dich:

> Prüf, ob es eine neue Version der Grundregeln gibt, und zeig mir, was sich geändert hat.
