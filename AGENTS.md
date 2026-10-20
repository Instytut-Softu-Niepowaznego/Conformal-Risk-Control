# AGENTS.md

Wytyczne dla agentów (i ludzi) pracujących w tym repozytorium.

## Projekt

Projekt z przedmiotu Rozpoznawanie wzorców, temat nr 17: kontrola ryzyka
pominięcia etykiet za pomocą Conformal Risk Control (Angelopoulos i in., ICLR 2024).
Repozytorium jest naszym opracowaniem i interpretacją publikacji, nie oficjalną
implementacją autorów. Szczegóły są w `README.md` i `topic.pdf`.

- Dokumenty piszemy po polsku, w formie bezosobowej („odtworzono”, „porównano”).
- Dokumenty LaTeX kompilujemy przez `latexmk -pdf <plik>.tex`. Kompilacja powinna
  przechodzić bez błędów i bez ostrzeżeń typu `Overfull \hbox`.

## Commity: Conventional Commits

Wszystkie commity stosują [Conventional Commits 1.0.0](https://www.conventionalcommits.org/pl/v1.0.0/):

```
<typ>[(zakres)][!]: <opis>

[treść]

[stopka]
```

- **Typ** po angielsku, małymi literami:
  - `feat`: nowa funkcjonalność (np. nowy eksperyment, nowa metoda)
  - `fix`: poprawka błędu
  - `docs`: dokumenty, raporty, deklaracja, slajdy, README
  - `refactor`: zmiana kodu bez zmiany zachowania
  - `perf`: wydajność
  - `test`: testy
  - `build`: zależności i środowisko
  - `ci`: konfiguracja CI
  - `chore`: pozostałe prace porządkowe (np. `.gitignore`)
  - `style`: formatowanie bez zmiany treści
- **Zakres** jest opcjonalny i opisuje obszar zmiany, np. `declaration`, `report`,
  `slides`, `crc`, `data`, `experiments`.
- **Opis** po polsku, w trybie rozkazującym, z małej litery, bez kropki na końcu,
  do ok. 72 znaków.
- **Treść** jest opcjonalna. Wyjaśnia *dlaczego*, nie *co*, i jest oddzielona
  pustą linią.
- **Zmiany łamiące** oznaczamy przez `!` po typie lub zakresie albo stopką
  `BREAKING CHANGE: ...`.
- Jeden commit to jedna logiczna zmiana.

Przykłady:

```
docs(declaration): uzupełnij harmonogram etapów
feat(crc): dodaj kalibrację z poprawką n/(n+1)
fix(experiments): zachowaj ziarno losowania między uruchomieniami
chore: dodaj .gitignore dla artefaktów LaTeX
```
