----
title: Nauka JavaScript od podstaw (1)
date: 2018/06/05
----

Małe opóźnienie z wpisem na blogu, ale z braku czasu nie dałem rady. Przepraszam za opóźnienia! :)

Jak wiecie zaczałem naukę 'czystego' `JavaScript-u`. Jak przebiegał powtórny etap tejże nauki?

# Co to jest JavaScript?
`JavaScript` to interpretowany, skryptowy język programowania.

Co to oznacza, że `interpretowany`? *INTERPRETOWANY* ponieważ plik, który nie jest kompilowany, jedynie zostanie  zinterpretowany przez program np. przez przeglądarkę i zostanie on wykonany jako np. odtwarzacz video albo galeria zdjęć.

# Co możemy stworzyć za pomocą JavaScriptu:
* odtwarzacz video
* kalkulator
* chat
* gry
* edytory tekstu

# Jak złapać kontekst użycia JavaScriptu na stronie?
Rozumiem to tak. Załóżmy, że posiadamy miniaturkę zdjęcia z wakacji. Jeśli najadę na zdjęcie myszką, i ustawie *`hover`* w stylach `CSS` to zdjęcie mi sie podświetli. Analogia do JavaScriptu, to taka według mnie, że jeśli najedziemy myszką na zdjęcie,nastepnie klikniemy, to wywołamy `zdarzenie`, które np. będzie polegało na wyświetleniu dużego zdjęcia obok miniatury.

# JQuery `=!` JavaScript ?
jQuery to inaczej zbiór funkcji napisanych w czystym JavaScript. Dzięki jQuery możemy manipulować drzewem DOM.

Osobiście spotkałem się z innymi opiniami na ten temat. Sporo osób mi mówiło `Czarek, zacznij od jQuery` inni zaś `Czarek, zacznij od czystego JavaScript, bo to podstawa do zrozumienia wszystkich innych framework'ów`.

Przez to wszystko do tej pory mam jeden wielki mętlik...
Patrząć z perspektywy problemu w zrozumieniu i pojęciu JavaScript-u, może ma to sens? Jak myslicie? Dajcie znać o swoich opiniach na ten temat! :-)


# JavaScript poza przeglądarką?
* `nodeJS` (programy napisane w nim to np. `Gulp`, `Grunt`, `Yeoman`
* `mongoDB` - zapytania w tej bazie wypisujemy za pomocą poleceń JavaScript.
* `Adobe Photoshop` - oznacza to, że rozszerzenia do programu zostały napisane własnie w JavaScript.

# Gdzie umieszczać skrypty JavaScript?
a) możemy jes umieszczać w elemencie `HEAD:
```
<script>
    alert('Witaj, Cezary!');
</script>
```
 Powyższy sposób nie powinien być praktykowany, ponieważ podczas otwarcia strony internetowej, pierw wczyta nam się skrypt, a nie reszta strony w postaci tekstu, obrazków



b) ... albo będziemy umieszczać w dowolnym miejscu w `BODY`, czyli tak zwane podlinkowanie skryptu:

Podlinkowanie wygląda następująco: `<script src="js/scripts.js"></script>`

* Dobrą praktyką jest umieszczanie skryptow na końcu, najlepiej przed zamykającym znacznikiem `body`, czyli `</body>`

### Dlaczego?
Jeśli umieścimy go w `head` to skryptsie wykonana, a póki co strona www nie zostanie wczytana, wykona się później.


# No więc czym jest `ZMIENNA`?
* zmienne są to podstawowe konstrukcje języka JavaScript - to ABSOLUTNA PODSTAWA!!!

Deklarowanie zmiennej wygląda następująco:
```
var imie = 'Cezary';
```

`var` - to słowo kluczowe języka JavaScript

`imie` - to nazwa zmiennej

`=` - jest to znak przypisania zmiennej

`Cezary` - jest to wartość mojej zmiennej

Innym sposobem deklaracji zmiennej jest:
```
var imie = 'Cezary`,
    nazwisko = 'Tworzewski';
```

### Co się dzieje ze zmienną, gdzie ona jest?
* wszystkie zmienne zostają zapisane w pamięci `RAM - Random Access Memory`

### Co mogą przechowywać zmienne?
* wartości prymitywne (np. ciąg znaków)
* referencje do obiketów (np. Date)
* referencje do funkcji


Ta lekcja minęła dość łatwo, wszystko z niej rozumiem do tej pory. Nie miałem żadnych trudności z poruszanymi zagadnieniami do tej pory. Bardzo możliwie, że dlatego, że nie raz uczyłem się tego - jest to dla mnie zrozumiałe.
Te początkowe lekcje chciałbym przerobić w miarę szybko, ale nie za szybko. Nie chciałbym pominąć żadnych ważnych kwestii, które porusza autor kursu.

Może kiedyś coś pominąłem, coś bardzo prostego? Może dlatego mam problem? Sam nie wiem. Nie jest to czas ani miejsce, żeby się rozwodzić nad tym tematem.
Szukam jakiegoś ratunku już dla siebie.

Wiem jedno - muszę baaaardzo dużo pracować / uczyć się!!!!

Blogowanie dopiero zaczynam więc...
bardzo dziękuje za doczytanie mnie do końca!!!