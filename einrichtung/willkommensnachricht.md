# Willkommensnachricht für neue Kollegen

Vorlage für die Nachricht, mit der eine neue Person ins Team kommt. Wer die Kollegen einlädt, sagt seinem Claude:

> Schreib mir aus `firma/einrichtung/willkommensnachricht.md` die Nachricht für [Vorname]. Füll alle Platzhalter aus, die du kennst, frag mich nach dem Rest, und nimm die Variante, die zu unserem Abgleich passt.

Platzhalter stehen in eckigen Klammern. Oben steht die Variante für Git (GitHub, Gitea, Forgejo), die Abweichungen für Cloud-Speicher stehen am Ende.

---

Hallo [Vorname],

ab sofort arbeitest du bei uns mit Claude, und zwar mit unserem Firmenordner. Darin steht alles, was Claude über [Firmenname] wissen muss: unsere Leistungen, Preise, unser Schreibstil und wie wir arbeiten. Dadurch klingen Angebote, Mails und Texte von Anfang an nach uns, und du musst Claude nicht jedes Mal alles neu erklären.

Die Einrichtung dauert etwa eine Viertelstunde. Claude macht das meiste selbst.

**1. Zugänge annehmen**

Du hast zwei Einladungen per Mail bekommen. Nimm beide an:

- die Einladung zu Claude Team von [Firmenname],
- die Einladung zur GitHub-Organisation [Name der Organisation]. Falls du noch keinen GitHub-Account hast, legst du dabei einen kostenlosen an.

**2. Claude installieren**

Lade die Claude Desktop-App von claude.com/download herunter, installiere sie und melde dich mit dem Konto an, das du gerade für Claude Team eingerichtet hast. Mehr musst du nicht selbst installieren.

**3. Deinen Arbeitsordner anlegen**

Leg einen leeren Ordner an, zum Beispiel „Claude“ in deinem Benutzerordner. Wichtig: nicht in OneDrive, iCloud oder Dropbox, diese Dienste vertragen sich nicht mit unserem Firmenordner. Der Ordner gehört nur dir, die anderen sehen ihn nicht.

Öffne in der Desktop-App den Bereich für Code und wähle diesen Ordner aus. Falls dir dort eine Option für eine abgetrennte Arbeitskopie angeboten wird (Worktree), lass sie ausgeschaltet. In so einer Kopie fehlt der Firmenordner.

**4. Den Startprompt abschicken**

Kopier diesen Text in Claude und schick ihn ab. Claude fragt zwischendurch nach Erlaubnis und führt dich einmal durch die Anmeldung bei GitHub im Browser. Unter Windows kann zusätzlich ein Fenster kommen, ob ein Programm Änderungen an deinem Gerät vornehmen darf. Das kannst du bestätigen, es geht um Git und die GitHub CLI.

> Richte diesen Ordner als meinen Arbeitsordner für den Firmenordner von [Firmenname] ein. Ich bin [Vorname] [Nachname], meine geschäftliche E-Mail ist [E-Mail], und ich arbeite bei [Firmenname] als [Rolle]. Wenn ein Schritt nicht klappt, hör auf und erklär mir in einfachen Worten, was los ist, statt weiterzumachen. Geh so vor:
>
> 1. Prüf, ob dieser Ordner in OneDrive, iCloud, Dropbox oder einem anderen Sync-Dienst liegt. Wenn ja, hör auf und sag mir, wohin ich ihn verschieben soll.
> 2. Prüf, ob Git und die GitHub CLI installiert sind, und installier, was fehlt. Unter Windows nimm dafür winget und sag mir vorher, dass gleich eine Rückfrage von Windows kommen kann.
> 3. Melde mich mit der GitHub CLI über den Browser bei GitHub an und richte Git so ein, dass es diese Anmeldung nutzt. Hinterleg für Git meinen Namen und meine E-Mail von oben.
> 4. Hol das Repo [Name der Organisation]/[Name des Firmenordners] als Unterordner `firma/` in diesen Ordner.
> 5. Leg eine CLAUDE.md an. Darin steht, wer ich bin (Name und Rolle von oben), dass das Firmenwissen in `firma/` liegt, und die Zeile `@firma/CLAUDE.md`, damit die Regeln des Firmenordners immer geladen sind.
> 6. Richte in `.claude/settings.json` dieses Ordners einen SessionStart-Hook ein, der beim Start jeder Sitzung den neuesten Stand holt: `git -C firma pull --rebase --autostash`. Schlägt das fehl, soll die Meldung bei dir ankommen, damit du mir Bescheid sagen kannst.
> 7. Verknüpf jeden Skill aus `firma/.claude/skills/` einzeln mit `.claude/skills/` in diesem Ordner, damit die Team-Skills sofort verfügbar sind. Unter Windows nimm dafür eine Verzeichnis-Verknüpfung, die keine Adminrechte braucht.
> 8. Leg die Ordner `notizen/` und `projekte/` für meine eigenen Sachen an.
> 9. Mach aus diesem Ordner ein eigenes privates Repo in meinem GitHub-Account und lade es hoch. `firma/` und `.env` werden darin ausgeschlossen. So ist mein Arbeitsordner gesichert, ohne dass ihn jemand anderes sieht.
> 10. Erklär mir zum Schluss in drei Sätzen, was du eingerichtet hast.

**5. Kurz testen**

Schließ Claude einmal und öffne deinen Ordner neu, damit alles geladen wird. Dann stell diese drei Fragen:

> Was weißt du über unsere Firma und unsere Angebote?

> Welche Skills stehen mir zur Verfügung?

> Schreib mir ein kurzes Angebot für einen Workshop bei einem neuen Kunden.

Wenn die Antworten nach [Firmenname] klingen, ist alles richtig eingerichtet. Wenn Claude nur Allgemeines sagt, schreib mir kurz.

**Vier Regeln für den Alltag**

1. Was nur dich betrifft, gehört in deinen Arbeitsordner, nicht in den Firmenordner. Alles im Firmenordner sehen alle.
2. Angebote, Projekte und Notizen legst du in `firma/arbeit/` an, das geht direkt. Das Firmenwissen änderst du nicht selbst. Wenn dort etwas falsch ist oder fehlt, sag Claude „schlag das dem Team vor“.
3. Wenn du Claude etwas über die Firma beibringst, fragt er, ob er es dem Team vorschlagen soll. Sag ja, dann haben alle etwas davon.
4. Wenn du mit einer Arbeit fertig bist, sag Claude „lad das hoch“. Meistens macht er das schon von selbst, so gehst du sicher, dass nichts nur auf deinem Rechner liegt.

Kundendaten wie Name, Funktion und geschäftliche Mail von Ansprechpartnern sind im Firmenordner in Ordnung. Daten über Mitarbeiter, Bewerber, Gesundheit, Privatkunden oder Bankdaten gehören nicht hinein. Claude weist dich darauf hin, falls so etwas auftaucht.

Bei Fragen meld dich jederzeit.

[Dein Name]

---

## Abweichungen bei SharePoint oder einem anderen Cloud-Speicher

Statt der GitHub-Einladung bekommt die Person eine Freigabe für den Firmenordner. Diesen synchronisiert sie auf ihren Rechner und stellt ihn auf „Immer auf diesem Gerät behalten“ (OneDrive) oder „Spiegeln“ (Google Drive).

Im Hinweis zu Schritt 4 entfällt der Satz über die Rückfrage von Windows. Im Startprompt ändern sich diese Schritte:

> 2. und 3. entfallen.
> 4. Der Firmenordner liegt unter [Pfad zum synchronisierten Ordner]. Verknüpf ihn mit diesem Ordner, sodass er hier als `firma/` erscheint.
> 6. entfällt, der Cloud-Speicher gleicht den Firmenordner selbst ab.
> 9. Sichere diesen Ordner, falls gewünscht, in [persönlicher Speicherort], aber ohne `firma/`.

Regel 4 für den Alltag entfällt ebenfalls.

Schritt 1 des Startprompts bleibt: Der Arbeitsordner selbst liegt auch hier nicht im Sync-Ordner, nur der Firmenordner.
