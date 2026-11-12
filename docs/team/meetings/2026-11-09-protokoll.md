# Meeting-Protokoll 09.11.2026

**Kontext:** Seminartermin — Betreuer-Feedback zum Workflow-Entwurf, Fokus Anforderungserhebung, Implementierungs- und Test-Workflow
**Beteiligte:** Team + Betreuer

---

## 1. Leitgedanke: KI als Katalysator

Zentrale Aussage des Termins:

> **KI wirkt als Katalysator für Engineering.** Bei schlechten Grundlagen, Workflows oder Prozessen verstärkt die KI auch die negativen Aspekte.

Konsequenzen:
- In **Greenfield-Projekten** ist es einfacher, gute Prozesse herauszuarbeiten und zu etablieren — saubere Grundlage von Anfang an.
- Der **Engpass wandert ins Review.** Nicht das Schreiben von Code ist der Flaschenhals, sondern dessen Prüfung und Freigabe.
- **Business-Aspekt ins Zentrum rücken** — der fachliche/geschäftliche Nutzen steht über der rein technischen Umsetzung.

**Beobachtung aus der Praxis:** Bei Unternehmen, die KI einsetzen, dominieren **Coding und Dokumentation** als Anwendungsfelder.

---

## 2. Anforderungserhebung

Offener Diskussionspunkt: Der konkrete Prozess zur Anforderungserhebung für unser Projekt ist noch **zu allgemein / nicht klar genug**.

**Konsentierte Richtung:**
- Anforderungen entstehen aus dem **Zerlegen des Produktkonzepts** (Dekomposition top-down).
- **Mehr ins Doing kommen:** mehrfaches Durchlaufen des Workflows, um Dinge iterativ anzupassen — statt einmaligem Vorab-Durchspezifizieren.
- **User Stories kleinteiliger** schneiden und **weniger spezifizieren** — die richtige Story-Größe ist noch zu bestimmen.
- **Autonomiegrad vorerst niedrig halten:** zunächst weniger stark automatisieren, später stärker, sobald sinnvoll und funktionsfähig.
- **Spezifikations-Schleife Agent ↔ PO:** iterativer Austausch bei der Spec-Ausarbeitung, solange bis die Anforderungen stimmen (Status „sehr gut" erreicht). Spätere Änderungen werden ergänzt, nicht vorweggenommen.

**Zu prüfen / anzuschauen:**
- **SWE-Bench** — als Referenz für Aufgabenzuschnitt und Bewertung.
- **Google DORA-Report** — Engineering-Metriken und Praxiserkenntnisse.
- Bericht analysieren und herausarbeiten, **bei welchen Aufgaben KI in unserem Projekt sinnvoll eingesetzt** werden kann.

---

## 3. Implementierungs- und Test-Workflow

**Prozessmodell:**
- **Keine Grundsatzdebatte Kanban vs. Scrum** — das jeweils Sinnvolle aus beiden Prozessen herausziehen.
- **Explizite Freigabe** nötig: Wann ist eine Story fertig zur Implementierung, und in welcher Reihenfolge wird implementiert? (Kein „nicht ready" ohne definierten Ready-Zustand.)

**Specs vs. Issues:**
- Versionierung von Issues ist **nicht nötig.**
- Deshalb erneut abzuwägen: reine **Anforderungen** als Issues erfassen → daraus per KI **Specs / Entwurfspläne** ableiten. Specs sind damit doch sinnvoll zu diskutieren.

**Git-seitige Gestaltung:**
- **Gestaggte Pull Requests** anschauen zur Separation von Tests: erst **Test-Branch mit PR**, dann **Implementierungs-Branch** auf dem PR des Test-Branch.
- **Signierte Commits.**
- **Versteckte Abnahmetests** sicher ablegen, sodass der Agent keinen Zugriff darauf hat → **separater Ordner mit speziell im Harness konfigurierten Zugriffsrechten.**

**Skills:**
- Einen **Skill zum Aufsetzen von Skills** erstellen.
- **Nicht zu viele Skills** — und Skills **selbst schreiben.**
- **Edge-Cases / Grenzfälle ableiten** und darauf basierend **Tests schreiben.**

---

## 4. Review & Sicherheitsbewertung von PRs

- **Review vor PR.**
- **Schwellenbewertung für Sicherheit:** Wie sicher ist ein PR? Definieren, was für den Menschen so aufbereitet wird, dass er es sinnvoll beurteilen kann — und was autonom/sicher einfach als „grün" markiert werden kann.
- **Kritikalitäts-Einstufung des PR in high / medium / low** nach zwei Achsen:
  1. **Unsicherheitsgrad**
  2. **Schweregrad / Impact**
- **GitHub Copilot Code Review** als Referenz anschauen.

---

## 5. Nächste Schritte

- **Workflow implementieren** (konkret in die Umsetzung gehen, mehrfach durchlaufen).
- **Anforderungen validieren** über **Oberflächen-MVPs** — Wireframes / Mockups.
- **Usability testen und validieren.**
- **Für nächsten Termin:** Fragen aus der eigenen Implementierung mitbringen; recherchieren, was andere im Unternehmen bereits ausprobiert haben und was funktioniert hat bzw. nicht.

---

## 6. Offene Aktionspunkte

| Aufgabe | Priorität |
|---|---|
| Konkreten Anforderungserhebungs-Prozess für unser Projekt schärfen (Produktkonzept-Dekomposition) | Hoch |
| Gestaggte PRs (Test-Branch → Impl-Branch) als Git-Workflow evaluieren | Hoch |
| Harness-Ordner mit Zugriffsrechten für versteckte Abnahmetests einrichten | Hoch |
| PR-Kritikalitäts-Schema (Unsicherheit × Impact → high/med/low) ausarbeiten | Mittel |
| Specs-aus-Issues-Ableitung vs. reine Issues abwägen und entscheiden | Mittel |
| Skill zum Aufsetzen von Skills erstellen | Mittel |
| SWE-Bench, DORA-Report, GitHub Copilot Code Review sichten | Mittel |
| Oberflächen-MVPs / Wireframes zur Anforderungsvalidierung bauen | Mittel |
| Fragen aus eigener Implementierung für nächsten Termin sammeln | Niedrig |
