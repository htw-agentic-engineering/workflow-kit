# Team Charta

**Projekt:** Projektseminar Agentic Engineering, WS 2026/27, HTW Dresden
**Betreuung:** Prof. Jürgen Anke, Ricardo Bochnia
**Stand:** 20.10.2026
**Version:** 0.2 (Entwurf)

> Diese Charta ist unsere gemeinsame Vereinbarung über Zusammenarbeit, Kommunikation und Arbeitsweise. Sie gilt erst, wenn alle Mitglieder unten zugestimmt haben. Änderungen werden im Team besprochen und als Commit mit dem Typ `docs` festgehalten.

## 1. Team und Rollen

| Name | Rolle | Erreichbar über |
|------|-------|-----------------|
| Etienne | Scrum Master | Discord |
| Nataliia | Product Owner | Discord |
| Tom | Developer | Discord |
| Thanh Loan | Developer | Discord |
| Paul | Developer | Discord |
| Rico | Developer | Discord |

Rollen können im Laufe des Semesters getauscht werden. Ein Tausch wird im Montagstermin abgesprochen und hier eingetragen.

## 2. Gemeinsames Ziel

Wir entwickeln eine Art Framework für das Arbeiten mit Agenten. Dabei suchen wir einen Weg, die Umgebung so aufzusetzen, dass effizientes und gezieltes Arbeiten möglich ist.

Nachfolgende Studierende sollen von unseren Erkenntnissen profitieren und ein Nachschlagewerk erhalten, wie agentische Methoden funktionieren können.

## 3. Kommunikation und Transparenz

Grundsatz: **Lieber einmal zu viel Bescheid sagen als einmal zu wenig.** Niemand wird für ein Problem, eine Frage oder eine Abwesenheit verurteilt. Problematisch ist nur, wenn das Team davon nichts erfährt.

### 3.1 Kanäle

| Kanal | Wofür |
|-------|-------|
| Discord, allgemeiner Kanal | Absprachen, Fragen, Abwesenheiten |
| Discord, GitHub Kanal | Automatische Repo Logs (Commits, Pull Requests, Issues) |
| GitHub Issues | Aufgaben, Bugs, technische Diskussionen zu einer konkreten Aufgabe |
| Montagstermin (Präsenz, HTW) | Wochenrückblick, Planung der neuen Woche, Klärung offener Punkte |

### 3.2 Probleme und Unklarheiten

* Wer bei einer Aufgabe nicht weiterkommt, meldet sich **spätestens nach 24 Stunden** im Discord, statt allein festzustecken.
* Unklarheiten zu Aufgabenstellung, Anforderungen oder Code werden offen gefragt. Es gibt keine dummen Fragen.
* Kann eine Aufgabe absehbar nicht bis zur Deadline erledigt werden, wird das **sofort** mitgeteilt, damit das Team umplanen kann.
* Technische Probleme zu einer konkreten Aufgabe werden zusätzlich im zugehörigen GitHub Issue dokumentiert, damit die Lösung später nachvollziehbar ist.

### 3.3 Abwesenheiten

* Geplante Abwesenheiten (Urlaub, Prüfungen, Arbeit, Termine) werden **so früh wie möglich, mindestens 24 Stunden vorher** im Discord angekündigt.
* Kurzfristige Ausfälle (Krankheit o. Ä.) werden gemeldet, sobald es möglich ist.
* Wer abwesend ist, sagt dazu, welche eigenen Aufgaben betroffen sind und ob jemand übernehmen muss.
* Gründe muss niemand nennen. Es reicht der Zeitraum und die Auswirkung auf die Aufgaben.

### 3.4 Reaktionszeit

Nachrichten im Discord, die das Team direkt betreffen, werden innerhalb von **24 Stunden** beantwortet, auch wenn es nur ein kurzes „gesehen“ ist.

## 4. Wochenrhythmus und Deadlines

| Tag | Was passiert |
|-----|--------------|
| Montag | Präsenztermin an der HTW: Rückblick, Aufgabenverteilung für die Woche |
| Dienstag bis Samstag | Bearbeitung der Aufgaben |
| **Samstag, 23:59 Uhr** | **Interne Deadline:** Alle Aufgaben der Woche sind fertig und gepusht bzw. als Pull Request eingereicht |
| Sonntag | Review Tag: Jedes Mitglied kann die Ergebnisse der anderen ansehen und Feedback geben |

Regeln dazu:

* Die interne Deadline ist **Samstag 23:59 Uhr**, auch wenn die offizielle Abgabe später liegt. Ziel ist, dass jeder theoretisch den Sonntag hat, um über die Arbeit der anderen zu schauen.
* Aufgaben werden nicht erst kurz vor der Deadline begonnen. Zwischenstände dürfen und sollen früher gepusht werden.
* „Fertig“ bedeutet: Die Definition of Done (Abschnitt 6) ist erfüllt.
* Feedback aus dem Sonntag Review wird zeitnah eingearbeitet.

## 5. Aufgabenverwaltung

* Jede Aufgabe ist ein GitHub Issue mit klarer Beschreibung und einer verantwortlichen Person.
* Der Fortschritt wird in GitHub Projects mit den Spalten **Todo / In Progress / Review / Done** gepflegt.
* Wer eine Aufgabe übernimmt, weist sich das Issue selbst zu, damit nichts doppelt bearbeitet wird.

## 6. Definition of Done

Eine Aufgabe gilt als erledigt, wenn:

* [ ] die Anforderungen aus dem Issue erfüllt sind
* [ ] der Code gepusht ist und die Commits den Konventionen aus Abschnitt 7 folgen
* [ ] Tests vorhanden sind und erfolgreich laufen
* [ ] Dokumentation bzw. README angepasst sind
* [ ] ein Pull Request erstellt und von mindestens einer anderen Person geprüft wurde
* [ ] das Issue geschlossen bzw. verlinkt ist

## 7. Git Konventionen

### 7.1 Commit Nachrichten

Wir verwenden **Conventional Commits 1.0.0** ([Spezifikation](https://www.conventionalcommits.org/de/v1.0.0/)).

Aufbau:

```
<typ>[optionaler scope]: <beschreibung>

[optionaler Textkörper]

[optionale Fußzeilen]
```

Erlaubte Typen:

| Typ | Verwendung |
|-----|------------|
| `feat` | Neue Funktion |
| `fix` | Fehlerbehebung |
| `docs` | Nur Dokumentation |
| `style` | Formatierung, keine Logikänderung |
| `refactor` | Umbau ohne neue Funktion und ohne Bugfix |
| `test` | Tests hinzufügen oder ändern |
| `chore` | Wartung, Abhängigkeiten, Konfiguration |
| `ci` | CI/CD Pipelines |
| `build` | Build System |
| `perf` | Performance Verbesserung |
| `revert` | Rücknahme eines früheren Commits |

Unsere Regeln:

* Typen werden **klein geschrieben**.
* Die Beschreibung ist **eindeutig und konkret**: Was wurde geändert? Nicht „fix stuff“ oder „update“.
* Sprache der Beschreibung: **Englisch**, einheitlich im ganzen Repo.
* Ein Commit enthält **eine** logische Änderung. Passt ein Commit zu mehreren Typen, wird er aufgeteilt.
* Breaking Changes werden mit `!` nach dem Typ/Scope oder mit der Fußzeile `BREAKING CHANGE:` markiert.
* Bezug auf Issues über Fußzeile, z. B. `Refs: #12`.

Beispiele:

```
feat(agent): add retry logic for SAIA API calls
fix(parser): handle empty response from tool call
docs: add setup guide for OpenCode
refactor(api)!: rename endpoint /run to /execute

BREAKING CHANGE: clients must use /execute instead of /run
Refs: #23
```

### 7.2 Branches und Pull Requests

* `main` ist geschützt, es wird nicht direkt darauf gepusht.
* Branch Namen sind frei wählbar, sollten aber aussagekräftig sein.
* Jede Änderung kommt über einen Pull Request mit Verweis auf das Issue.
* Mindestens **eine** Person reviewt, bevor gemergt wird.
* Merge Strategie: **Merge Commit**.

## 8. Entscheidungen

* Entscheidungen werden möglichst im Konsens getroffen.
* Gibt es keinen Konsens, entscheidet die einfache Mehrheit. Bei Gleichstand entscheidet der Product Owner.
* Wichtige Entscheidungen (Architektur, Tools, Aufgabenverteilung) werden schriftlich unter `docs/decisions/` festgehalten.

## 9. Werkzeuge

| Zweck | Tool |
|-------|------|
| Kommunikation | Discord |
| Code und Versionierung | GitHub Organisation (zwei Repositories) |
| Aufgaben | GitHub Issues und GitHub Projects |
| KI / Agenten | OpenCode mit SAIA API (GWDG / KISSKI) |
| Dokumentation | Markdown im Repository |

## 10. Zustimmung

Mit dem Eintrag bestätigt jedes Mitglied, die Charta gelesen zu haben und sich daran zu halten.

| Name | Datum | Zugestimmt |
|------|-------|------------|
| Etienne | | ☐ |
| Nataliia |20.10.2026 | ☑  |
| Tom | | ☐ |
| Thanh Loan | | ☐ |
| Paul | | ☐ |
| Rico | 20.10.2026 | ☑ |

## Änderungshistorie

| Version | Datum | Änderung |
|---------|-------|----------|
| 0.1 | 19.10.2026 | Erster Entwurf |
| 0.2 | 20.10.2026 | Platzhalter ersetzt, Formatierung bereinigt, Abschnitt Konflikte entfernt |
