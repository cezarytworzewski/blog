---
title: Nauka JavaScript od podstaw (1)
date: 2018/06/05
---

Małe opóźnienie z wpisem na blogu, ale z braku czasu nie dałem rady.
Przepraszam za opóźnienia! :)

Jak wiecie zacząłem naukę 'czystego' `JavaScript-u`. Jak przebiegał
powtórny etap tejże nauki?

## Co to jest JavaScript

`JavaScript` to interpretowany, skryptowy język programowania.

Co to oznacza, że `interpretowany`? _INTERPRETOWANY_ ponieważ plik,
który nie jest kompilowany, jedynie zostanie  zinterpretowany przez
program np. przez przeglądarkę i zostanie on wykonany jako np. odtwarzacz
video albo galeria zdjęć.

## Co możemy stworzyć za pomocą JavaScriptu

* odtwarzacz video
* kalkulator
* chat
* gry
* edytory tekstu

## Jak złapać kontekst użycia JavaScriptu na stronie

Rozumiem to tak. Załóżmy, że posiadamy miniaturkę zdjęcia z wakacji.
Jeśli najadę na zdjęcie myszką, i ustawie `hover` w stylach `CSS` to
zdjęcie mi się podświetli. Analogia do JavaScriptu, to taka według mnie,
że jeśli najedziemy myszką na zdjęcie, następnie klikniemy, to wywołamy
`zdarzenie`, które np. będzie polegało na wyświetleniu dużego zdjęcia
obok miniatury.

## JQuery `=!` JavaScript

jQuery to inaczej zbiór funkcji napisanych w czystym JavaScript. Dzięki
jQuery możemy manipulować drzewem DOM.

Osobiście spotkałem się z innymi opiniami na ten temat. Sporo osób mi
mówiło

> Czarek, zacznij od jQuery

 inni zaś
 > Czarek, zacznij od czystego
JavaScript, bo to podstawa do zrozumienia wszystkich innych framework'ów`.

Przez to wszystko do tej pory mam jeden wielki mętlik w głowie...
Patrząc z perspektywy problemu w zrozumieniu i pojęciu JavaScript-u,
może ma to sens? Jak myślicie?

Dajcie znać o swoich opiniach na ten temat! :-)

## JavaScript poza przeglądarką

* `Node.js` (programy napisane w nim to np. `Gulp`, `Grunt`, `Yeoman`
* `MongoDB` - zapytania w tej bazie wypisujemy za pomocą poleceń JavaScript.
* `Adobe Photoshop` - oznacza to, że rozszerzenia do programu zostały
    napisane właęnie w JavaScript. Przykładem będzie `plugin`
    [Piotra Kowalskiego][piecioshka]) o nazwie
    [*`Photoshop Plugin Copy Color After Picking`*][plugin]

## Gdzie umieszczać skrypty JavaScript

* możemy je umieszczać w elemencie `head`:

    ```html
    <script>
        alert('Witaj, Cezary!');
    </script>
    ```

    Powyższy sposób nie powinien być praktykowany, ponieważ podczas otwarcia
    strony internetowej, pierw wczyta nam się skrypt, a nie reszta strony w
    postaci tekstu, obrazków.

* albo będziemy umieszczać w dowolnym miejscu w `body`, czyli tak zwane
    podlinkowanie skryptu:

    ```html
    <script src="scripts/main.js"></script>
    ```

Dobrą praktyką jest umieszczanie skryptów na końcu, najlepiej przed
zamykającym znacznikiem `body`, czyli `</body>`

Dlaczego?

Jeśli umieścimy go w `head` to skrypt się wykonana, a na razie strona www
nie zostanie wczytana, wykona się później. Obejściem na to może być
dodanie atrybutu `async`, które opóźnia proces interpretowania kodu.

## No więc czym jest `ZMIENNA`

Zmienne są to podstawowe konstrukcje języka JavaScript - ABSOLUTNA PODSTAWA!

Deklarowanie zmiennej wygląda następująco:

```js
var imie = 'Cezary';
```

* `var` - to słowo kluczowe języka JavaScript
* `imie` - to nazwa zmiennej
* `=` - jest to znak przypisania zmiennej
* `Cezary` - jest to wartość mojej zmiennej

Innym sposobem deklaracji zmiennej jest:

```js
var imie = 'Cezary',
    nazwisko = 'Tworzewski';
```

## Gdzie jest zapisywana wartość zmiennej

Wszystkie zmienne zostają zapisane w pamięci `RAM - Random Access Memory`

## Co mogą przechowywać zmienne

* wartości prymitywne (np. ciąg znaków)
* referencje do obiektów (np. Date)
* referencje do funkcji

Ta lekcja minęła dość łatwo, wszystko z niej rozumiem do tej pory.
Nie miałem żadnych trudności z poruszanymi zagadnieniami do tej pory.
Bardzo możliwie, że dlatego, że nie raz uczyłem się tego - jest to dla
mnie zrozumiałe.
Te początkowe lekcje chciałbym przerobić w miarę szybko, ale nie za szybko.
Nie chciałbym pominąć żadnych ważnych kwestii, które porusza autor kursu.

Może kiedyś coś pominąłem, coś bardzo prostego? Może dlatego mam problem?
Sam nie wiem. Nie jest to czas ani miejsce, żeby się rozwodzić nad tym
tematem. Szukam jakiegoś ratunku już dla siebie.

Wiem jedno - muszę baaaardzo dużo pracować / uczyć się!

Blogowanie dopiero zaczynam więc... bardzo dziękuje za doczytanie mnie do końca!

[piecioshka]: https://twitter.com/piecioshka
[plugin]: https://github.com/piecioshka/photoshop-plugin-copy-color-after-picking
