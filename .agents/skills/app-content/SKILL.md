---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

Explainer „Zahlen unter null“ (Mathematik, Klassen 7-8, Strang `mathematik/arithmetik`), ein Kapitel `zahlen-unter-null`. Die gemeinsamen Regeln aller Mathe-Explainer (Schreibweisen, Aufgaben, Quellen) stehen im Epic lernapps/apps#402; die wichtigsten sind unten übernommen.

## Curriculum

Mathematik, Sekundarstufe I, Klassen 7-8 (Jahrgang laut Lernlandkarte; `rationale-zahlen` steht dort in 5-6, wird hier mit dem Rechnen zusammen in 7-8 geübt). Die Reihenfolge gibt die Lernlandkarte Mathematik (`https://lernapps.net/apps/map/mathematik/`), nicht ein Lehrplan. KMK-Bildungsstandards 2022 und der Hessische Lehrplan wurden nicht geöffnet (nicht geprüft). Kein eigenes Material des Auftraggebers.

## Competencies

Kapitel `zahlen-unter-null`:
- `rationale-zahlen` – „Ich kann mit negativen Zahlen, Gegenzahlen und Beträgen umgehen und sie an Beispielen wie Temperatur erklären.“ Seiten `negative-zahlen`, `ordnen`, `gegenzahl-betrag`.
- `rationale-zahlen-rechnen` – „Ich kann mit negativen Zahlen rechnen und dabei Vorzeichen- und Klammerregeln beachten.“ Seiten `addieren-subtrahieren`, `multiplizieren`, `dividieren`, `bruch-dezimal`.
- Wiederholt, nicht geübt (Seite `recap`, `recap:`): `natuerliche-zahlen` (Natürliche Zahlen im Stellenwertsystem), `brueche-multiplizieren-dividieren` (Bruchrechnung: Multiplikation und Division).
Aufgaben-ids stehen in den Seitendateien `src/zahlen-unter-null/<seite>.yaml`.

## Content structure

- Seitenreihenfolge: `recap`, `negative-zahlen`, `ordnen`, `gegenzahl-betrag`, `addieren-subtrahieren`, `multiplizieren`, `dividieren`, `bruch-dezimal`.
- Abschnitts-ids auf jeder geübten Seite gleich, in dieser Reihenfolge: `einstieg` (Nachrichten der Klasse und erste Aufgabe), `beispiel`, `merke`, `uebung`; Titel sagen, was der Abschnitt auf der Seite tut. Höchstens 350 Wörter Text, mindestens vier Aufgaben, Aufgaben steigen von Erkennen zu Anwenden.
- Recap: Kopf „Das brauchst du für dieses Kapitel“, je Baustein ein Abschnitt (Name wie auf der Karte), Fachbegriffe fett mit Zahlenbeispiel, je Baustein eine `Kurztest`-Komponente und der Satz mit Name und Kartenseite des Bausteins, Schluss „Du bist bereit, wenn du …“. Keine Aufgaben (Schema).
- Geschichte: Die siebte Klasse betreut eine Messstation (Thermometer, Höhe über dem Meer, Materialkasse). Jede Seite beginnt mit zwei bis drei Nachrichten; Namen erfunden und gemischt: Jule, Karim, Mara, Tomás. Keine Marken, keine realen Personen.

## Terminology

- **Zahlengerade** (nie „Zahlenstrahl“) ab Seite `negative-zahlen`; dort wird gesagt, dass der Zahlenstrahl ein linkes Ende bekommt. Auf der Recap-Seite steht „Zahlenstrahl“ nur, wenn es um Zahlen ab 0 geht, und wird dort erklärt.
- Minus immer `−` (U+2212), nie `-`. Negative Zahlen in Rechnungen in Klammern: `5 + (−3)`. Mal `·`, geteilt `:`, Dezimalkomma, Einheiten mit geschütztem Leerzeichen (`3 °C`, `20 €`), Brüche gesetzt (`\frac`). Große Zahlen ab 5 Stellen in Dreiergruppen mit schmalem geschütztem Leerzeichen, vierstellig ohne.
- Wörter: negative Zahl, positive Zahl, Vorzeichen, Gegenzahl, Betrag, kleiner/größer, Zahlengerade. Glossar (`definition`): Zahlengerade, negative Zahl, Vorzeichen, Gegenzahl, Betrag; für das Recap zusätzlich Stellenwert, Bruch, Kürzen, gleichnamig machen, Dezimalzahl.
- Anrede „du“, kurze Sätze, kein „man“ in Arbeitsaufträgen.
- Keine Formelbefehle außerhalb der Liste der Laufzeit; in Überschriften keine geschützten Leerzeichen oder gruppierten Zahlen.

## Exercise patterns

- **Ablesen und Einordnen**: `single-choice`/`number` mit Zahlengerade-Bild (`figure image`), `alt` nennt nur Gegebenes. Variiert: Kontext (Thermometer, Kontostand, Meeresspiegel).
- **Ordnen/Vergleichen**: `ordering`, `true-false` mit Begründung in `explanation`.
- **Gegenzahl/Betrag**: `generated`, Fehlertyp „Minus einfach weggelassen“.
- **Rechnen** (`generated`): Zahlen gezogen, `where` ohne Nulldivision, Fehlertypen `mistakes` mit Meldung (Vorzeichen vergessen, Beträge statt Zahlen subtrahiert, „minus mal minus gleich minus“, Betrag statt Zahl geteilt). Antwort als Zahl; Brüche als Bruch oder Dezimalzahl, wo die Aufgabe das sagt. Jede Aufgabe mit Rechenprobe (Test der Laufzeit über feste Seeds, plus Stichprobe von Hand).
- **Zahlenmuster**: `table` mit Zeilen `3 · 2`, `3 · 1`, `3 · 0`, `3 · (−1)`; Regel erst danach in `merke`.
- Beispiel: `src/zahlen-unter-null/negative-zahlen.yaml` (Musterseite).
- Jede Frage verlangt `links`: wir verlinken nur die Kartenseite des Bausteins (`https://lernapps.net/apps/map/mathematik/c/<id>/`), keine externen Seiten (Regel des Epics).
- Der Selbsttest im Recap ist die Komponente `Kurztest` (Kopie der gemeinsamen Vorlage, `src/components/Kurztest.*`): eine Frage, eine Auswahl, Rückmeldung mit Grund, nichts gezählt; genau eine Option richtig; `nojs` nennt Frage, Optionen und Antwort.

## Figures

- Zahlengerade als eigene SVG in `src/images/` (`source: eigene Zeichnung`, `licence: CC0-1.0`): gleiche Abschnitte, Hauptstriche beschriftet, die Null hervorgehoben, Pfeilspitzen an beiden Enden, die Beschriftung „negative Zahlen“/„positive Zahlen“ trägt die Information (nie Farbe allein), Textfarbe `currentColor` für den Dunkelmodus. `alt` sagt, was die Zeichnung zeigt; `caption` sagt, worauf man achten soll. Das Bild zeigt nur Gegebenes, nie die gesuchte Zahl.
- Pfeile für Addieren/Subtrahieren: gleiche Gerade, Pfeil nach rechts für Addieren eines Positiven, nach links für Subtrahieren eines Positiven; Anfang und Ende beschriftet.
- Breite: lesbar bei 360 px (viewBox 640 breit, höchstens 11 beschriftete Striche).

## Sources

Lernlandkarte Mathematik (geöffnet und gelesen), eigene Herleitungen und eigene Aufgaben. Nichts aus Schulbüchern oder Arbeitsblättern; keine Wikipedia-Links; keine Dritt-Inhalte. Alle Rechnungen vom fachlichen Prüfer nachgerechnet.

## Adding a chapter or round

1. Kompetenz-id und „Ich kann …“-Satz aus der Karte nehmen, Seite in `src/zahlen-unter-null/<id>.yaml` mit `competencies: [id]`.
2. Abschnitte `einstieg`, `beispiel`, `merke`, `uebung` wie oben, Aufgaben nach den Mustern.
3. Seite in `pages` der `chapter.yaml` eintragen (Lesereihenfolge); neues Kapitel in `chapters` der `src/app.yaml`.
4. Schreibweisen gegen den Abschnitt „Terminology“ prüfen.
5. `npx vp check --fix`, `npx --no -- lernapps check`, committen.

## Rules learned from mistakes

None yet.
