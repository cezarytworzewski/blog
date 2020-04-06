---
title: Nauka JavaScript od podstaw (2)
date: 2018/06/13
---

Ogólnie rzecz biorąc, zaczynam od początku **JavaScript**, ale mnóstwo
rzeczy wiem - _tak czuję, albo wydaję mi się!_

Dzisiaj skupie się na tekstowym typie danych `String`,
typie liczbowym `Number`, `true`, `false` i wartości
`true` & `false`. A dzisiejsza przygodę zakończę z `null` vs. `undefined`.

## Tekstowy typ danych `String`

Warto powiedzieć, że tekstowy typ danych zapisujemy za pomocą apostrofów
 `' '` albo cudzysłowów `" "`. Jest to obojętne jaką konwencje użyjemy,
ale zawsze powinniśmy stosować tylko jedną. Między innymi po to,
aby nasz kod był czytelny dla nas, ale również dla naszych kolegów po fachu.

Zadeklarujemy sobie zmienną `firstName`:

```js
let firstName = 'Jan';
```

Stworzyliśmy właśnie zmienną `firstName` i przypisaliśmy do niej wartość `Jan`.

Żeby sprawdzić jaki typ danych ma nasza zmienna używamy to takich działań
operatora `typeof`.

`typeof firstName` => Wynikiem jest: ***String***

Dlatego jeśli wartość naszej zmiennej posiada `'  '` albo `"  "` to wiem,
że jest to typ ***String***.

Tekstowy typ danych to *String*.

## Przykłady

```javascript
let firstName = 'Jan';
let lastName = "Kowalski";
```

Załóżmy, że mamy tytuł książki albo cytat. Zazwyczaj umieszczamy je w `" "`.
Jak to zrobić w JavaScript?

```javascript
let bookTitle = "Władca pierścieni"
```

Wywołuję sobie to w konsoli przeglądarki. Wynik to:

```text
    bookTitle // wywołuję sobie zmienną
    "Władca Pierścieni" // jest to wynik, posiada cudzysłowy, ale są to cudzysłowy informujące, że wartośc jest String,
```

Żeby zrobić cudzysłów określający tytuł książki to robię to tak:

```javascript
let bookTitle = "'Władca Pierścieni'";
```

albo:

```js
let bookTitle = '"Władca Pierścieni"';
```

inny sposób to:

```js
let bookTitle = "\"Władca Pierścieni\"";
```

## Liczbowy typ danych Number

**Number** to liczbowy typ danych, dzięki nim możemy przechowywać liczby,
wartości liczbowe, liczby całkowite czy wartości zmiennoprzecinkowe.
Zapisujemy je troszkę inaczej niż `String` tzn. zapisujemy je bez użycia
cudzysłowów.

* liczba całkowita:

    ```js
    let number = 20;
    ```

* liczba zmiennoprzecinkowa:

    ```js
    let number = 20.5;
    ```

    Do tworzenia liczb zmiennoprzecinkowych używamy **kropki**.

W JavaScript mamy też zmienne (stałe), czyli **Infinity** i **-Infinity**:

* `Infinity` => 1.797693134862315E+308
* `-Infinity` => 1.797693134862316E+308

Posiadamy również taką wartość jak `NaN` (_Not a Number_):

* to nie jest wartość liczbowa, jest tylko skojarzona jako typ liczbowy
* jeśli będziemy robić jakieś obliczenia, a wynikiem nie będzie nowa liczba,
    to zostanie zwrócona wartość `NaN`.

## Prawda, fałsz, wartości true & false

```js
let isLoggedIn = true;

if (isLoggedIn) {
    console.log('Zalogowano');
} else {
    console.log('Nie zalogowano');
}
```

to jest bardzo istotna linia: `if (isLoggedIn)` w środku nawiasu
**zawsze** jest prawda. To nie musi być zmienna `isLoggedIn`, może to
być dowolna inna zmienna. Zgodnie z wartością zmiennej `isLoggedIn`
zmienna ta ma wartość `true`, później w **instrukcji warunkowej**
sprawdzam czy `isLoggedIn` jest prawdziwe. Jeśli prawdziwe to wykonam
kod `console.log('Zalogowano');`

## Wartości fałszywe to

* false
* 0
* " "
* null
* undefined
* NaN

Przykład:

```js
let value = 0;

if(value) {
    console.log('Ta wartość nie jest fałszywa');
} else {
    console.log('Wartość jest fałszywa');
}
```

## null vs. undefined

Są to wartości fałszywe! - ale nie oto teraz chodzi.

`let yourName;` Sprawdzam swoją zmienną za pomocą `typeof`, czyli
`typeof yourName`. Wynikiem jest `"undefined"`. Jeśli się odwołamy
bezpośrednio do zmiennej w konsoli, czyli wpiszemy: `yourName;` to wynik
również wskazuje na `undefined`

Jedno `undefined` posiada cudzysłowy a drugie nie w powyższym opisie.
Musimy pamiętać, że:

Operator `typeof` _zawsze_ zwraca `String`, ale wartość tego String
jest `undefined`.

Jeśli utworzymy zmienną, ale nie przypiszemy do niej żadnej wartości,
to ma ona wartość `undefined`: `let yourName;` - wartość zmiennej to
*`undefined`*

Jeśli, chcemy **z góry**, aby zadeklarowana zmienna miała wartość pustą
to przypiszemy do niej wartość **null**: `let yourName = null;`

Sprawdźmy jedną rzecz: `typeof null` - zwróci nam `object`, ale **STOP**

***null* NIE JEST OBIEKTEM**

### Jak to ma się do obiektów

`let person = {};`, sprawdźmy za pomocą `typeof person.name` =>
Wynik to: `"undefined"`

Dlaczego tak jest?

Ponieważ próbujemy się odwołać do czegoś, czego nie ma. W tym wypadku
próbujemy się odwołać do właściwości name obiektu person`

Jeśli chcę, aby ta właściwość była pusta to możemy zrobić to tak:

```js
let person = {
    name: null
};
```

Teraz `typeof person.name` będzie miał wartość `object`.

Jeśli wynikiem kiedyś będzie `null`, to muszę pamiętać, że zmienna
została już zadeklarowana, ale nic nie zostało do niej przypisane.
Przy `undefined` wartość nigdy nie została ustawiona.

## Podsumowując

Lekcja ta, też nie była dla mnie skomplikowana. Wydaje mi się, że
rozumiem o co w niej chodzi. Wykonałem parę ćwiczeń wraz z
**Piotr Palarz** i jestem zadowolony :-)

Jeżeli popełniłem jakieś błędy w opisie lekcji, albo uważacie, że nie
bardzo jednak to rozumiem, to proszę  dajcie znać w komentarzach!

***Pozdrawiam! :-)***
