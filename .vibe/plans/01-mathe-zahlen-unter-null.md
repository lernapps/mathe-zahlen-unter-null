---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: {}
---

# Plan: mathe-zahlen-unter-null, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-23. Explore, Plan, Code, Commit.*

## Goal

Lernende der Klassen 7-8 verstehen, dass die Zahlengerade über die Null nach links weiterwächst, ordnen negative Zahlen, geben Gegenzahl und Betrag an und rechnen mit rationalen Zahlen (Vorzeichen- und Klammerregeln). Sie leiten die Regeln an Bewegungen auf der Zahlengerade und an fortgesetzten Zahlenmustern her.


<!-- 1–2 sentences: what learners do, what they learn. -->

## Key decisions

- Archetyp: `explainer` (Auftrag im Issue lernapps/apps#768; Seiten erklären, dazwischen Aufgaben; Zahlengerade als Bild, `generated` für Rechenaufgaben).
- Strang `mathematik/arithmetik`, Format 2. Ein Kapitel.
- Schicht 2, Tiefe 3; Abhängigkeiten: #385 und #389 (Baustein `brueche-multiplizieren-dividieren`), beide in Schicht 1. Veröffentlichen erst nach deren Veröffentlichung oder auf Freigabe des Orchestrators.
- „Zahlengerade“ (nicht „Zahlenstrahl“) auf allen Seiten; Skala mit gleichen Abschnitten, Hauptstriche beschriftet (Konvention aus #385). Minus immer `−` (U+2212), negative Zahlen in Rechnungen in Klammern.
- Sprache: nur Deutsch (guess: das Issue nennt keine zweite Sprache).
- Geschichte (guess): leicht, als kurze Nachrichten einer Klasse in einem Wetter-/Höhenprojekt; Namen erfunden. Entscheidung fällt im Plan.
- `scope`: nicht nötig (keine `open-task`, kein Material des Auftraggebers).
- Look: vom Archetyp festgelegt (ruhig wie ein Arbeitsblatt, Dunkelmodus folgt dem Gerät).


<!-- One line each: decision and reason. Archetype first. Your own choice without the creator: mark "(guess)". -->

## Notes

- Fach/Strang: Mathematik, `arithmetik` („Zahl und Operation“). Karte gelesen (`mathematik.json`, 129 Kompetenzen).
- Kompetenzen des Kapitels 1 „Zahlen unter null“ (Stufe 7-8):
  - `rationale-zahlen` – „Ich kann mit negativen Zahlen, Gegenzahlen und Beträgen umgehen und sie an Beispielen wie Temperatur erklären.“ (5-6, Schritt 2, öffnet 27, bisher von keiner App geübt)
  - `rationale-zahlen-rechnen` – „Ich kann mit negativen Zahlen rechnen und dabei Vorzeichen- und Klammerregeln beachten.“ (7-8, Schritt 1, öffnet 26, bisher von keiner App geübt)
- Voraussetzungen von außen (`requires`): `natuerliche-zahlen` (Natürliche Zahlen im Stellenwertsystem) und `brueche-multiplizieren-dividieren` (Bruchrechnung: Multiplikation und Division). Beide kommen in eine Sammel-Wiederholung nach regeln.md Abschnitt 7; keine Apps anderer Explainer gelesen, kein Link dorthin, nur die Kartenseiten.
- Bestand: keiner, Repo war leer. Beide Bausteine fehlen.
- Seitenschnitt (Vorschlag): Recap · Negative Zahlen auf der Zahlengerade · Ordnen und Vergleichen · Gegenzahl und Betrag · Addieren und Subtrahieren als Bewegung · Multiplizieren (Zahlenmuster über die Null) · Dividieren · Vorzeichen- und Klammerregeln mit Brüchen und Dezimalzahlen. Eine Kompetenz je Seite; `rationale-zahlen` drei Seiten, `rationale-zahlen-rechnen` vier.
- Übung (Muster aus lernapps-exercise-patterns, Mathematik): Ablesen/Einordnen auf der Zahlengerade (Bild plus `generated`), Ordnen (`ordering`), Wahr/Falsch mit Begründung, berechnen mit `generated` und diagnostizierten Fehlern (Vorzeichen vergessen, Beträge statt Zahlen subtrahiert, „Minus mal Minus = Minus“).
- Wie Lernende dorthin kommen: Addieren/Subtrahieren durch Schritte auf der Zahlengerade, Malnehmen durch Fortsetzen von Mustern (3·2, 3·1, 3·0, 3·(−1) …), Teilen als Umkehrung des Malnehmens. Fehlvorstellungen, die die Rückmeldung fängt: „−5 > −2, weil 5 > 2“, Betrag = „Minus weglassen“ auch bei Rechnungen, Vorzeichenregeln auswendig vermischt, Minus als Rechenzeichen und Vorzeichen verwechselt.
- Umfang: drin: ganze, Bruch- und Dezimalzahlen links der Null, Ordnen, Betrag, Gegenzahl, die vier Grundrechenarten. Draußen: Terme mit Variablen (#393), Wurzeln/irrationale Zahlen (#392), Brüche und Dezimalzahlen als solche (#389), Potenzen mit negativer Basis. Wertebereich: ganze Zahlen mit Beträgen bis 100 (Rechnen) bzw. bis 1000 (Meeresspiegel, Kontostand), Brüche mit Nennern bis 12, Dezimalzahlen mit höchstens zwei Stellen; nie still enger.
- Quellen: Lernlandkarte Mathematik (geöffnet, gelesen). KMK-Bildungsstandards 2022 und Hessischer Lehrplan: nicht geöffnet (nicht nötig, die Karte gibt die Reihenfolge); nicht geprüft. Keine zweiten Quellen, keine Formulierungen übernommen; alle Aufgaben eigene, mit Rechenprobe.
- Hinweise zur Arbeitsweise: Beim Abarbeiten der Explore-Aufgaben habe ich Aufgaben 3 bis 6 abgehakt, bevor ich die Skill-Dateien gelesen hatte; ich habe sie danach nachgelesen. Ein Tick lässt sich mit `lernapps plan` nicht zurücknehmen.


<!-- Strand or subject, competencies by chapter (ids), didactic approach, scope, sources and licences, open questions. -->

### Review

**Lernenden-Prüfer (Unteragent, Klasse 7), Musterseite `negative-zahlen`, vor der Meldung:**
- Umgesetzt: Balken am Thermometer benannt; falsche Zahl im Feedback „−6 °C“ korrigiert; „Vorzeichen“ erst nach seiner Einführung; „Abschnitt“ erklärt; `mistakes` für die Zahlaufgabe (3, −2); Punkt C jetzt in einer Mehrfachauswahl; einleitender Satz vor dem Bild der Aufgaben; Feedback der generierten Aufgabe passt zu „im Minus“ und „unter dem Meeresspiegel“; Bildunterschrift „weiter links = kleiner“ entfernt (gehört auf `ordnen`, ein Schritt je Seite); Verlängerung des Zahlenstrahls nach links im Text benannt.
- Nach dem Prüferlauf geändert (inhaltlich, also noch einmal zu prüfen): genau diese Stellen, plus die Recap-Seite (neu, noch nie von einem Prüfer gesehen).
- Zweiter Lauf (Recap und Musterseite): Recap: Einer/Zehner/Hunderter, Erweitern, Kehrbruch und der Sprung 3/4 → 75/100 ergänzt, zweiter Kurztest je Baustein, Satz „Hattest du den Kurztest nicht richtig …“ gekoppelt; Musterseite: „Vorzeichen“/„Rechenzeichen“ im Merke erklärt, `mistakes` für −5 und 0. Nach diesem Lauf nur diese Änderungen; sie sind nicht noch einmal von einem Prüfer gesehen (offen).
- Zusätzliche Laufzeit-Funde: Kasten „Wiederholung“ und Titel doppelt, Link-Text der Recap-Verknüpfung zeigt Rohbezeichner (`mathematik/natuerliche-zahlen`), unvollständige Mehrfachauswahl meldet nicht, ob die gewählten stimmen.
- Offen / Laufzeit (nicht von mir behoben, Funde): Antwort wird mit „-“ statt „−“ angezeigt; Meldung bei ungültiger Eingabe nennt „ordne zu“ und sagt nichts zur Zahleneingabe; `true-false` und `number` melden allgemein „Lies dazu noch einmal den Text“; Aufgabennummer beginnt zufällig; „Neue Aufgabe“ nur als Symbol; Link „Mehr dazu“ führt auf die Kartenseite (gewollt) mit der Beschriftung der Frage.
- `lernapps check`: Hinweise `explainer-repetition` und `explainer-text-load` auf der Recap-Seite bleiben bewusst (Ich-kann-Sätze in Kopf und Checkliste nach regeln.md §7; Begriffe als Definitionen).
- Zählung `a/b` in Komponenten-Rückmeldungen (regeln.md §2): Kurztests Brüche und Dividieren im Recap, je Frage und Optionen mit Infos (ca. 14 Stellen).

## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [x] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [x] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [x] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [x] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [x] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [x] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [x] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [x] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [x] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [x] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [x] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [x] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.
      Creator: Orchestrator (in Vertretung des Menschen): Recherche freigegeben, Seitenschnitt, Fehlertypen, Chat-Geschichte, nur Deutsch, nur Karte als Quelle ok. Recap ohne Aufgaben plus eigene Kurztest-Seite; Zahlenstrahl wird auf Seite 1 zur Zahlengerade; Musterseite Negative Zahlen auf der Zahlengerade.

### Answers

- Goal: laut Issue lernapps/apps#768 (Leitidee und Kapitel); der Orchestrator antwortet für den Menschen.
- Learners: Mathematik, Klassen 7-8; kennen natürliche Zahlen, Brüche und Dezimalzahlen und das Malnehmen und Teilen von Brüchen.
- Model and focus: Zahlengerade als tragende Darstellung (Issue: Didaktik).
- Look and feel: fixed by the archetype.
- Content: Claude, aus der Lernlandkarte, eigene Aufgaben (regeln.md Abschnitt 4).
- Amount: ein Kapitel, beide Bausteine (Issue).
- Languages: Deutsch (guess).


<!-- The interview: per topic the creator's answer, in their words. Keep the topics. -->

- Goal: what learners do in the app, what they learn.
- Learners: subject, school year, prior knowledge.
- Model and focus: an app of the catalog (https://lernapps.net/apps/llms.txt) as model; what matters most (exercises,
  visualisations, game feel).
- Hurdles: misconceptions and mistakes of the learners; the creator's examples and experiments.
- Content: who writes it (creator, you, from sources); own material (worksheets, tests).
- Amount: how much content in the first version; what comes later.
- Languages: German only, or German and English. Never English only.
- Look and feel: calm like a worksheet, or like a game (colours, praise, effects); dark mode.
- Terms: the creator's words for the main things in the app, used everywhere.
- Finding the app: what teachers and parents would search for.

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [x] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [x] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [x] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [x] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [x] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [x] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: Orchestrator (in Vertretung): Plan bestätigt, weiter mit Musterseite negative-zahlen, vorher Lernenden-Prüfer Klasse 7. Kurztest-Komponente aus /tmp/epic/docs/mathe-epic/components/.

### Content method

**Aufbau.** Ein Kapitel `zahlen-unter-null`, Strang `mathematik/arithmetik`, nur Deutsch. Seiten in der Reihenfolge der `requires`:

| Nr | Seite (id) | Kompetenz | Voraussetzung, die die App nicht übt |
|---|---|---|---|
| 1 | `recap` „Das brauchst du hier“ (`recap:` beide) | – | `natuerliche-zahlen`, `brueche-multiplizieren-dividieren`: Abschnitt je Baustein, Fachbegriffe fett mit Beispiel (Stellenwert, Bruch, Kürzen, gleichnamig machen, Dezimalzahl), Kopf und Checkliste, keine Aufgaben |
| 2 | `kurztest` „Das brauchst du hier – Kurztest“ | siehe Offen | wie Seite 1; je Baustein 1-2 Kurzaufgaben, Satz mit Name und Kartenseite des Bausteins |
| 3 | `negative-zahlen` (Musterseite) | `rationale-zahlen` | `natuerliche-zahlen` (Recap) |
| 4 | `ordnen` | `rationale-zahlen` | – |
| 5 | `gegenzahl-betrag` | `rationale-zahlen` | – |
| 6 | `addieren-subtrahieren` | `rationale-zahlen-rechnen` | – |
| 7 | `multiplizieren` | `rationale-zahlen-rechnen` | – |
| 8 | `dividieren` | `rationale-zahlen-rechnen` | `brueche-multiplizieren-dividieren` (Recap) |
| 9 | `bruch-dezimal` Vorzeichen- und Klammerregeln mit Brüchen und Dezimalzahlen | `rationale-zahlen-rechnen` | `brueche-multiplizieren-dividieren` (Recap) |

Baustein → Seite: `rationale-zahlen` → 3, 4, 5; `rationale-zahlen-rechnen` → 6, 7, 8, 9. Abschnitts-ids auf jeder Seite gleich: `einstieg`, `beispiel`, `merke`, `uebung`.

**Änderung Recap (Orchestrator, regeln.md §7 Punkt 6).** Der Selbsttest steht als Komponente `Kurztest` direkt in der Recap-Seite (`recap:`), nicht auf einer eigenen Seite: eine Frage, eine Auswahl, Rückmeldung mit Grund, nichts gezählt oder gespeichert, Tastatur und Textalternative für die Version ohne JavaScript. Vorlage: `src/components/Kurztest.*` im Repo `lernapps/mathe-saetze-entdecken`, Branch `work`; Komponente kopieren und anpassen. Damit entfällt Seite 2 „Kurztest“ (8 Seiten, Nummern ab 3 rücken auf); Rückfall nur bei Fehlschlag: Kurztest-Seite direkt hinter dem Recap. Begründung für die Komponente (`prefer-built-in-block`): kein Block zeigt Aufgaben auf einer `recap:`-Seite.

**Zahlengerade.** Seite 3 führt sie ein: der Zahlenstrahl aus der Grundschule und Klasse 5-6 bekommt links ein Ende dazu, ab da heißt alles „Zahlengerade“. Skala mit gleichen Abschnitten, Hauptstriche beschriftet, die Null hervorgehoben, links negativ (Farbe nie allein: Beschriftung und Lage tragen die Information).

**Muster (Mathematik-Referenz).**
- Ablesen und Einordnen: SVG-Zahlengerade (`image`, eigene Dateien mit `alt`), dazu `generated` (Zahl ablesen/Temperatur, Kontostand, Höhe zu Meeresspiegel), Zeichnung zeigt nur Gegebenes.
- Ordnen/Vergleichen: `ordering`, `true-false` mit Begründung im Feedback.
- Gegenzahl/Betrag: `generated` mit Fehlertyp „Minus einfach weggelassen“ bei Gegenzahl; `matching` Zahl ↔ Betrag.
- Addieren/Subtrahieren: Pfeile als SVG, `generated` mit Klammerschreibweise `5 + (−3)`; Fehler: Vorzeichen des Ergebnisses, Subtrahieren eines Negativen als Subtrahieren des Betrags.
- Multiplizieren/Dividieren: Zahlenmuster als `table` (3 · 2, 3 · 1, 3 · 0, 3 · (−1) …), Regel danach in „Merke“; `generated` mit Fehlertyp „minus mal minus gleich minus“. Dividieren als Umkehrung des Malnehmens.
- Brüche/Dezimalzahlen: `generated` mit gesetzten Brüchen (`formula`), Antwort als Bruch oder Dezimalzahl, Rechenprobe im Selbsttest der Seite.
- Eine Komponente nur, wenn kein Block reicht (`prefer-built-in-block`): geplant keine; die Zahlengerade zum Anklicken wäre schön, ein `generated` mit Zahleneingabe prüft dasselbe. (guess)

**Datendateien.** `src/data/kontexte.yaml`: Kontexte für Aufgaben (Thermometer, Kontostand, Meeresspiegel) mit Einheit und erlaubtem Wertebereich, je Tatsache einmal.

**Hinweis für spätere Agenten.** Neue Seite: ein Abschnitt je id wie oben, Aufgaben nach Muster der Seite 3, Schreibweisen nach regeln.md Abschnitt 2; Seed-Prüfung der `generated`.

**Engagement je Seite.**
1. `recap`: erst „Kannst du das?“-Hinweis auf den Kurztest, dann Begriffe mit Beispiel. Wechsel: lesen, Beispielkasten. Ende: Checkliste.
2. `kurztest`: Einstieg ist schon eine Aufgabe; Rückmeldung nennt die Karte. Belohnung: klare Aussage, was sitzt.
3. `negative-zahlen`: Opening: Thermometer ablesen („Wie kalt ist es?“) vor der Erklärung; Chat der Klasse (Messstation) als Story; Gerade bekommt ein linkes Ende; Abschluss: Merke und nächste Frage „Was ist kälter?“.
4. `ordnen`: erst zwei Temperaturen vergleichen, dann Ordnen mit `ordering`; Merke: größerer Betrag ≠ größere Zahl bei negativen.
5. `gegenzahl-betrag`: Spiegelbild der Gerade um die Null; Betrag als Abstand von der Null; Belohnung: Betrag und Gegenzahl auf einen Blick.
6. `addieren-subtrahieren`: Opening: Kontostand um 20 € ändern; Pfeile; Regel danach.
7. `multiplizieren`: Opening: Muster fortsetzen; Regel aus dem Muster; Belohnung: Vorzeichenregel selbst hergeleitet.
8. `dividieren`: Opening: Umkehrprobe; Teilen als Umkehren des Malnehmens.
9. `bruch-dezimal`: Opening: Spiegelbild von 1/2 und 0,5; alles zusammen; Kapitelrückblick, nächste Schritte (Terme, Wurzeln, ohne Link).
Wiederholen nur mit anderer Form: Gerade → Tabelle → Rechnung.

**Geschichte (guess).** Eine siebte Klasse betreut eine kleine Messstation (Thermometer, Höhe, Kasse für Material); jede Seite beginnt mit zwei bis drei Nachrichten, Namen erfunden und gemischt, endet mit dem nächsten Schritt. Kein Kindchenschema.

**Offen.** (a) Der Kurztest übt `natuerliche-zahlen` und `brueche-multiplizieren-dividieren`, die die App nicht trägt; ob `competencies-on-map` und `recap-names-competencies` das erlauben, prüft `lernapps check` in Code (sonst Kurztest ohne Kompetenzeintrag oder `ahead`). (b) `\angle`, geschützte Leerzeichen und gruppierte Zahlen nicht in Überschriften.


<!-- One line each: the patterns and where; the figures and how they are made; the data files; each component, what it
checks and what it cannot; how a later agent adds a chapter. It becomes the content guide in Code. -->
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Musterseite negative-zahlen: Zahlengerade-SVG (Zahlenstrahl bekommt ein linkes Ende), Chat-Einstieg, Thermometer-Ablese-Aufgabe, Merke, mindestens vier Aufgaben mit diagnostizierten Fehlern; als Lernender (Klasse 7) durchspielen
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
- [ ] Recap (recap: beide Bausteine) und Kurztest: Begriffe fett mit Zahlenbeispiel (Stellenwert, Bruch, Kürzen, gleichnamig machen, Dezimalzahl), Checkliste; Kurztest mit 1-2 Aufgaben je Baustein und Satz mit Kartenseite
- [ ] Seiten ordnen und gegenzahl-betrag: Ordnen/Vergleichen, Gegenzahl als Spiegelbild, Betrag als Abstand, je mindestens vier Aufgaben
- [ ] Seiten addieren-subtrahieren und multiplizieren: Pfeile auf der Zahlengerade, Muster über die Null, generated mit Klammerschreibweise und Fehlertypen
- [ ] Seiten dividieren und bruch-dezimal: Umkehrung des Malnehmens, Vorzeichenregeln mit Brüchen und Dezimalzahlen, Kapitelrückblick
- [ ] Kontext-Datendatei, Glossar, Startseite und Kapitelbeschreibung; lernapps check ohne Fehler; Schreibweisen nach regeln.md Abschnitt 2 durchgehen
<!-- tasks: pages (5 added): the other pages or screens, after the pattern -->
- [ ] Update the content guide so that it describes the app as built (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
