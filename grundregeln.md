# Grundregeln für den Firmenordner

Version 1.0 vom 15. Oktober 2026. Quelle: https://github.com/Julian-Ivanov/firmenordner-vorlage

Diese Regeln beschreiben, wie die Arbeit mit dem Firmenordner funktioniert. Sie sind in jeder Firma gleich, die mit dieser Vorlage arbeitet. Was nur für eure Firma gilt, steht in der CLAUDE.md daneben. Wo die CLAUDE.md der Firma etwas anderes festlegt als diese Datei, gilt die CLAUDE.md der Firma.

## Wo was liegt

- `wissen/`: Firmenwissen, also Leistungen und Preise, Schreibstil, Abläufe, Kundengruppen. Bevor du etwas für die Firma schreibst, lies hier nach.
- `.claude/skills/`: Skills, die das ganze Team nutzt.
- `arbeit/`: laufende Arbeit, also Angebote, Kundenprojekte, Meeting-Notizen. Ein Unterordner pro Kunde oder Projekt.
- `vorschläge/`: Änderungswünsche an `wissen/`, an den Skills, an der CLAUDE.md und an dieser Datei.
- `einrichtung/`: Willkommensnachricht und Startprompt für neue Kollegen.

## Mit wem du arbeitest

Wer gerade mit dir arbeitet, steht in der CLAUDE.md ihres Arbeitsordners. Steht dort kein Name, frag nach und trag ihn dort ein. Den Namen brauchst du für Vorschläge und für die Beschreibung beim Hochladen.

## Was du direkt änderst und was nicht

`wissen/`, `.claude/skills/`, die CLAUDE.md der Firma und diese Datei änderst du nie direkt, auch nicht durch neue Dateien dort und auch dann nicht, wenn dich jemand ausdrücklich darum bittet. Stattdessen legst du einen Vorschlag an.

In `arbeit/` legst du Dateien direkt an und bearbeitest sie direkt.

Ausnahme Einrichtung: Steht in der CLAUDE.md der Firma `Einrichtung: läuft`, wird der Firmenordner gerade aufgebaut. Dann änderst du alles direkt. Erst bei `Einrichtung: abgeschlossen` gelten die Vorschläge.

## Vorschläge

Ein Vorschlag ist eine Datei in `vorschläge/` mit dem Namen `JJJJ-MM-TT-vorname-thema.md`, alles klein, das Thema in ein bis drei Wörtern mit Bindestrichen, zum Beispiel `2026-10-15-anna-tagessatz.md`. Gibt es im Team zwei Leute mit demselben Vornamen, hängst du die Initiale des Nachnamens an (`anna-m`). Legt die CLAUDE.md der Firma Bereiche mit eigenen Unterordnern fest, kommt der Vorschlag in den Unterordner des Bereichs, zu dem die betroffene Datei gehört.

Inhalt:

```
Betrifft: wissen/leistungen-und-preise.md (oder: neue Datei wissen/...)
Änderung: was sich ändern soll, möglichst als fertiger Text
Grund: ein bis zwei Sätze
Von: Vorname
```

Zeig der Person den Vorschlag kurz, bevor du ihn anlegst. Danach lädst du ihn sofort hoch.

Ist die Person selbst für die betroffene Datei zuständig, fragst du nach dem Anlegen gleich, ob du den Vorschlag einarbeiten sollst. So bleibt auch ihre Änderung im Verlauf nachvollziehbar.

## Durchsicht der Vorschläge

Wenn jemand sagt „geh die Vorschläge durch“:

1. Hol den neuesten Stand.
2. Nimm die Vorschläge, für die diese Person zuständig ist. Wer zuständig ist, steht im Frontmatter der betroffenen Datei unter `verantwortlich`. Fehlt der Eintrag oder geht es um eine neue Datei, gilt, was die CLAUDE.md der Firma dazu sagt.
3. Fass jeden Vorschlag in zwei Sätzen zusammen und sag dazu, ob er einer anderen Stelle im Firmenwissen widerspricht. Bei Skills erklärst du zusätzlich, was der Skill macht, ob er Befehle auf dem Rechner ausführt und auf welche Konnektoren er zugreift.
4. Warte pro Vorschlag auf ja, nein oder eine Änderung.
5. Freigegebene Vorschläge arbeitest du ein und setzt in der betroffenen Datei `geprüft_am` auf das heutige Datum. Erledigte und abgelehnte Vorschläge löschst du.
6. Lade alles hoch, mit einer Beschreibung wie „Chef: Durchsicht, Tagessatz übernommen, Checkliste übernommen“.

Einarbeiten darf nur, wer für die betroffene Datei zuständig ist. Fragt jemand anderes, zeigst du die Vorschläge nur an.

## Merk dir das

Wenn dich jemand bittet, dir etwas zu merken, und es die Firma betrifft (Preise, Leistungen, Abläufe, Kunden, Schreibstil), frag: „Soll ich das dem Team vorschlagen?“ Bei ja legst du einen Vorschlag an. Persönliches merkst du dir wie gewohnt nur für diese Person.

## Abgleich

Welcher Weg gilt, steht in der CLAUDE.md der Firma.

### Über Git (GitHub, Gitea, Forgejo)

- Beim Start jeder Sitzung holt eine Automatik im Arbeitsordner den neuesten Stand. Meldet sie einen Fehler, sag der Person in einem Satz, was los ist und dass sie gerade mit einem älteren Stand arbeitet. Gibt es keine Automatik, holst du den Stand selbst, bevor du im Firmenordner etwas liest oder schreibst.
- Hochladen machst du sofort, nach jedem neuen Vorschlag, wenn ein Stück Arbeit in `arbeit/` fertig ist, und nach jeder Durchsicht. Sag dabei kurz, was du hochlädst.
- Sagt jemand „lad das hoch“, „schick das ans Team“ oder etwas Ähnliches, prüfst du, was im Firmenordner noch nicht hochgeladen ist, und lädst es hoch.
- Jede Änderung bekommt eine kurze Beschreibung mit Namen, zum Beispiel „Anna: Vorschlag Tagessatz 1.400 Euro“ oder „Ben: Angebot K-MB Workshop“.
- Hat inzwischen jemand anderes etwas geändert, holst du zuerst dessen Stand und führst beide zusammen. Ist unklar, welche Fassung gilt, fragst du nach, statt eine zu verwerfen.
- Halbfertiges lädst du nur hoch, wenn die Person es ausdrücklich will.

### Über einen Cloud-Speicher (SharePoint, OneDrive, Google Drive, Dropbox)

- Der Ordner gleicht sich von selbst ab, Holen und Hochladen entfallen.
- Findest du Dateien mit einem Gerätenamen, „Konflikt“ oder „Kopie“ im Namen, sag Bescheid und benutze sie nicht. Auf Wunsch führst du sie mit dem Original zusammen und löschst die Kopie.
- Liegt eine Datei nur als Platzhalter vor und nicht vollständig auf dem Rechner, sag Bescheid, statt sie zu überschreiben.

## Kundendaten und Zugangsdaten

Erlaubt sind Geschäftskontakte: Firmenname, Ansprechpartner mit Name und Funktion, geschäftliche E-Mail und Telefonnummer. Nie in den Firmenordner gehören Daten über Mitarbeiter und Bewerber, Gesundheitsdaten, Daten von Privatkunden und Bankdaten. Wenn so etwas auftaucht, weise darauf hin und speichere es nicht.

Passwörter, Zugangsschlüssel und `.env`-Dateien gehören nie in den Firmenordner, sondern in den Arbeitsordner der jeweiligen Person.

## Frontmatter

Jede Datei in `wissen/` hat im Frontmatter `verantwortlich:` (Vorname) und `geprüft_am:` (Datum der letzten Prüfung).

## Neue Version der Grundregeln

Fragt jemand, ob es neue Grundregeln gibt, lädst du die aktuelle Fassung von https://raw.githubusercontent.com/Julian-Ivanov/firmenordner-vorlage/main/grundregeln.md und vergleichst die Versionsnummer. Ist sie neuer, fasst du die Änderungen in wenigen Sätzen zusammen und sagst, ob etwas davon mit dem Abschnitt „Bei uns anders“ in der CLAUDE.md der Firma kollidiert. Die neue Fassung übernimmst du erst nach einem Ja der Person, die laut CLAUDE.md der Firma für das Firmenwissen zuständig ist. Danach lädst du sie hoch.
