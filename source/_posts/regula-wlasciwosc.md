---
title: Czym się różni reguła od właściwości w CSS?
date: 2018/06/15
---

Pod lupę wezmę teraz `CSS`. Opowiem o tym, czym jest właściwość a czym
reguła w CSS.

## Co to jest reguła CSS?

Dzięki regułą CSS, możemy stworzyć wygląd, tak jakbyśmy chcieli aby nasza
strona wyglądała dla jednego, bądź wielu elementów.

Reguła CSS określa **wygląd** dla elementu HTML.

### Składnia reguły

Reguła CSS składa się z:

* selektora - selektor jest elementem HTML, który chcemy edytować, może
    to być element zdefiniowany jako klasa, wygląda to mniej więcej tak:
    Elementowi `h3` nadaję klasę: `<h3 class="size-title"></h3>`.
* nawiasu klamrowego {} - w danym nawiasie umieszczamy swoje parametry.
    Umieszczamy swoje operacje, czyli operacje, które będą coś zmieniać
    na mojej stronie od strony warstwy prezentacji
* właściwość - za ich pomocą określamy, co chcemy zmienić w naszej stronie
    internetowej, określamy jaki element HTML chcemy zmienić.
    Chcemy np. zmienić tło naszej strony internetowej. Za tło odpowiada
    właściwość `background-color`
* wartość - za pomocą wartości, określamy jak chcemy zmienić element, czy
    nadamy mu kolor czerwony.

#### Prosty przepis na stworzenie reguły CSS

```css
selektor {
    właściwość: wartość;
}
```

czyli, chce zmienić element `h3`, nadać mu wielkość czcionki o rozmiarze
25px. Gdzie moją **właściwością** jest *wielkość czcionki*:

```css
h3 {
    font-size: 25px;
}
```

Wyobraź sobie, że przed Tobą znajduje się stos białych, czystych kartek,
a Twoim zadaniem jest pokolorowanie każdej z nich. Dodatkowo każdą
kartkę koloru czerwonego musisz przeciąć na pół. Pierwsza czynność,
czyli pokolorowanie kartek, oczywiście nie jest niczym trudnym.
Druga czynność, czyli przecięcie na pół kartek koloru czerwonego,
wymaga od Ciebie odszukania danej kartki, czyli selekcji spośród danej
grupy kartek.

no więc:

* **regułą** - są tutaj kartki papieru,
* **właściwością** - jest tu informacja, że chcemy pokolorować, czyli
    właściwość *color*
* **wartość** - to już jest określony kolor, np. czerwony, zielony

Dlatego właściwość CSS, zawiera się w regule CSS, jest czymś podrzędnym,
bez czego selektor (reguła) CSS nie będzie działać.

Właściwości są niezbędne do poprawnego działania *reguły CSS*.

Mam nadzieję, że nie co przybliżyłem Wam różnicę pomiędzy *regułą*
a *właściwością* CSS.
