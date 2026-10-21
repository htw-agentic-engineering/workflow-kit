# <Projektname>

<!-- Diese Datei liest der Agent in jeder Sitzung. Kurz halten:
     nur, was er IMMER braucht. Details stehen in den verlinkten Dateien. -->

## Worum geht es
<!-- 2–3 Sätze. Details: docs/product/overview.md -->

## Befehle
- Tests: <!-- z. B. python -m pytest -->
- Starten: <!-- … -->
- Linting: <!-- … -->

## Struktur
- `src/presentation/` – Oberfläche bzw. API
- `src/application/` – Abläufe der Anwendungsfälle
- `src/domain/` – fachliche Begriffe und Regeln, ohne Abhängigkeit zu Datenbank oder Oberfläche
- `src/infrastructure/` – Datenbank und externe Dienste
- `tests/` – Tests, gespiegelt zur Struktur in `src/`

## Fachsprache
Verwende ausschließlich die Begriffe aus `docs/product/glossary.md` – in Code, Tests und Oberfläche.

## Arbeitsweise
- Lies vor einer Umsetzung die zugehörige Spezifikation in `docs/specs/`.
- Halte dich an die Entscheidungen in `docs/adr/`. Weiche nicht ohne Rückfrage davon ab.
- Bei größeren Aufgaben erst einen Plan vorlegen und auf Freigabe warten.
- Bei Unklarheiten nachfragen, nicht raten.
- Schreibe Tests für jedes Akzeptanzkriterium.

## Nie ohne Rückfrage
- Neue Abhängigkeiten hinzufügen
- Dateien löschen
- Spezifikationen oder ADRs ändern
