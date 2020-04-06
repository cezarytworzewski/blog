---
title: Jaka jest różnica pomiędzy znacznikiem img & background-image?
date: 2018/06/14
---

Wszystko zaczęło się od _chęci_ umieszczenia baneru na stronie www.
Tylko jak to poprawnie zrobić?

## Znacznik `img`

Znacznik `img` służy do dodawania  pliku graficznego do naszej strony
internetowej. Jest to znacznik samozamykający.
**Nie robimy czegoś takiego jak `</img>`**

Znacznik ten posiada również atrybuty:

* najważniejszy to atrybut `src` - gdzie pomiędzy cudzysłowy dodajemy
    ścieżkę do naszego obrazka,
* kolejny atrybut to `alt` - atrybut ten posiada alternatywny tekst
    dla naszego obrazka. Jeśli podamy złą ścieżkę do obrazka to wyświetli
    nam się **tekst alternatywny**,
    Atrybut `alt` możemy jeszcze spotkać w sytuacji, jeśli usuniemy nasz
    obrazek z serwera, a strona dalej będzie istnieć i odwoływać się do
    ścieżki na serwerze (oczywiście, tego obrazka już nie ma),
* atrybut `title` - jeśli najedziemy kursorem myszy na zdjęcie to
    pojawi się tekst obrazka
* kolejne atrybuty to `height` oraz `width`:
    +`height` - wysokość grafiki
    +`width` - szerokość grafiki

 Służą one do zmiany rozmiarów wyświetlającego obrazek.

* jeszcze inny atrybut to `align` - służy do wyrównywania obrazków w
    poziomie.

    +Atrybut `align` posiada dwie wartości:

        -`left`
        -`right`

Przykładowy kod z użyciem znacznika `img`:

## Reguła `background-image`

Reguła, ta ustawia obrazek tła dla elementu.

Wygląda to tak: `background-image: url(ścieżka-do-obrazka)`

Mamy stworzony kod `HTML`:

W pliku np. `style/main.css` odwołujemy się do reguły `background-image`
po to, aby dodać nasz długo oczekiwany baner:

### Wszystko ładnie, pięknie - ale kiedy stosować jedno albo drugie

Podchodząc do tworzenia projektu trzeba najpierw się zastanowić nad tym,
czy dane tło ma być takie samo na wszystkich podstronach czy nie.
**Musimy wiedzieć dlaczego chcemy użyć tej właściwości**

Jeśli dodamy plik za pomocą `CSS` to muszę pamiętać, że:

* będę mógł zmienić tryb wyświetlania w `background-image`, czyli ustawić
    `position` albo `repeat` lub `no-repat`
* jeśli nie planuję zmieniać baneru (grafiki) na stronie powinienem użyć
    `background-image`
* nie będę mógł zapisać grafiki jeśli kliknę prawym przyciskiem myszy
* nie będę mógł zaznaczyć obrazka

Jeśli dodam plik za pomocą znacznika `img` to muszę pamiętać, że:

* mogę zapisać obrazek za pomocą prawego przycisku myszy
* mogę zaznaczyć obrazek
* obrazek mogę dodać do każdej podstrony osobno, a później będę mógł w
    bardzo łatwy sposób podmienić grafikę gdzie chcemy

## Definicja `img` & `backgroung-image`

* `img` - to skrót od `images` (ang. _obrazek_)
* `background` (ang. _tło_)
* `background-image` - mogę przetłumaczyć jako `tło obrazkowe`

`img` służy do dodawania zdjęcia, obrazków, natomiast `background-image`
służy do dodawania tła na stronie
