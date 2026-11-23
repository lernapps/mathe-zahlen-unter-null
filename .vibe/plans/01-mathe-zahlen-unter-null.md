---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: explore
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
- [ ] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.

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

- [ ] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [ ] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [ ] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [ ] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [ ] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [ ] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [ ] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.

### Content method

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

- [ ] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [ ] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [ ] Load skill `lernapps-explainer`.
- [ ] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [ ] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
<!-- tasks: pattern: the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
<!-- tasks: pages: the other pages or screens, after the pattern -->
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
