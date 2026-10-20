# Conformal Risk Control: kontrola ryzyka pominięcia etykiet

Projekt z przedmiotu **Rozpoznawanie wzorców** (studia II stopnia), temat nr 17:
*Kontrola ryzyka pominięcia etykiet za pomocą Conformal Risk Control*.

## Czym jest to repozytorium

Repozytorium zawiera nasze opracowanie tematu, czyli to, jak sami rozumiemy
publikację bazową i jak odtwarzamy ją na małych danych:

> A. N. Angelopoulos, S. Bates, A. Fisch, L. Lei, T. Schuster.
> *Conformal Risk Control*. ICLR 2024.
> [arXiv:2208.02814](https://arxiv.org/abs/2208.02814) ·
> [kod autorów](https://github.com/aangelopoulos/conformal-risk-control)

To nie jest oficjalna implementacja autorów publikacji. Opisy, wyprowadzenia
i eksperymenty pokazują naszą interpretację metody CRC i jej uproszczoną adaptację
do zadania z kursu. Zmiany względem publikacji są dokumentowane na bieżąco.

## Pytanie badawcze

Jak wielkość zbioru kalibracyjnego wpływa na kontrolę ryzyka pominięcia prawdziwych
etykiet i na rozmiar zwracanych zbiorów predykcji?

W skrócie:
- syntetyczny problem wieloetykietowy (5 etykiet, 20 cech), klasyfikator OneVsRest
  z regresją logistyczną;
- CRC z docelowym ryzykiem α = 0,1 porównana ze stałym progiem 0,5;
- kalibracja na 50, 200 i 500 obiektach, po 30 losowań dla każdego rozmiaru.

## Zawartość

| Plik | Opis |
|------|------|
| `declaration.tex` / `declaration.pdf` | Deklaracja projektu: temat, opis zadania, harmonogram etapów |
| `topic.pdf` | Opis tematu z platformy kursu |

## Kompilacja dokumentów

Potrzebny jest TeX Live z pakietami `latexrecommended`, `latexextra`,
`fontsrecommended` i `langpolish`. Na Arch Linux:

```bash
sudo pacman -S --needed texlive-basic texlive-latex texlive-latexrecommended \
  texlive-latexextra texlive-fontsrecommended texlive-langpolish texlive-binextra
latexmk -pdf declaration.tex
```

## Autorzy

- [Imię i nazwisko autora 1]
- [Imię i nazwisko autora 2]
