---
title: Porównanie znaczników "q, cite, blockquote".
date: 2018/06/15
---

Postaram się teraz zrozumieć co łączy znaczniki `q`, `cite` oraz `blockquote`.

Jedyne co ich _łączy_ to to, że wszystkie służą do **CYTOWANIA**.

Ale pamiętajmy możemy cytować zdanie, kogoś, wiersz fragment z książki ale który
będzie odpowiedni w danym kontekście? Dlatego zacznę od znacznika `q`.

Znaczniki `q`, `cite` & `blockquote`:

* znacznik **q** - służy co cytowania krótszej wypowiedzi. Może być cytowane
    zdanie wypowiedziane przez kogoś np.

    ```html
    <p>
        Programiści powiadają, że <q>Każdy może nauczyć się programowania</q>.
        Zgadzam się z tym
    </p>
    ```

    lub

    ```html
    <p>
        Pani powiedziała, że <q>Dopilnuję, żeby nikt z Was nie zdał matury</q>.
        Nie powinna tak mówić.
    </p>

* znacznik **cite** - również służy do cytowania, ale cytowania w których
    odwołujemy się do innych źródeł. Mogą to być odwołania do pracy twórczej
    różnych autorów książek, profesorów, poetów np.

    ```html
    <p>
        Prawdą jest to, że <cite>Adam Mickiewicz</cite> wers
        <q>Litwo, Ojczyzno moja! ty jesteś jak zdrowie;</q>
    </p>
    ```

* znacznik **blockquote** - za pomocą tego znacznika zacytujemy dłuższy
    fragment tekstu, może to być artykuł z gazety, wiersz np.

    ```html
    <blockquote>
    Litwo, Ojczyzno moja! ty jesteś jak zdrowie;
    Ile cię trzeba cenić, ten tylko się dowie,
    Kto cię stracił. Dziś piękność twą w całej ozdobie
    Widzę i opisuję, bo tęsknię po tobie.
    Panno święta, co Jasnej bronisz Częstochowy
    I w Ostrej świecisz Bramie! Ty, co gród zamkowy
    Nowogródzki ochraniasz z jego wiernym ludem!
    Jak mnie dziecko do zdrowia powróciłaś cudem
    (— Gdy od płaczącej matki, pod Twoją opiekę
    Ofiarowany martwą podniosłem powiekę;
    I zaraz mogłem pieszo, do Twych świątyń progu
    Iść za wrócone życie podziękować Bogu —)
    Tak nas powrócisz cudem na Ojczyzny łono!...
    Tymczasem, przenoś moją duszę utęsknioną
    Do tych pagórków leśnych, do tych łąk zielonych,
    Szeroko nad błękitnym Niemnem rozciągnionych;
    Do tych pól malowanych zbożem rozmaitem,
    Wyzłacanych pszenicą, posrebrzanych żytem;
    Gdzie bursztynowy świerzop, gryka jak śnieg biała,
    Gdzie panieńskim rumieńcem dzięcielina pała,
    A wszystko przepasane jakby wstęgą, miedzą
    Zieloną, na niej zrzadka ciche grusze siedzą.
    </blockquote>
    ```

    czego wynikiem będzie:

```html
<blockquote>
    Litwo, Ojczyzno moja! ty jesteś jak zdrowie;
    Ile cię trzeba cenić, ten tylko się dowie,
    Kto cię stracił. Dziś piękność twą w całej ozdobie
    Widzę i opisuję, bo tęsknię po tobie.
    Panno święta, co Jasnej bronisz Częstochowy
    I w Ostrej świecisz Bramie! Ty, co gród zamkowy
    Nowogródzki ochraniasz z jego wiernym ludem!
    Jak mnie dziecko do zdrowia powróciłaś cudem
    (— Gdy od płaczącej matki, pod Twoją opiekę
    Ofiarowany martwą podniosłem powiekę;
    I zaraz mogłem pieszo, do Twych świątyń progu
    Iść za wrócone życie podziękować Bogu —)
    Tak nas powrócisz cudem na Ojczyzny łono!...
    Tymczasem, przenoś moją duszę utęsknioną
    Do tych pagórków leśnych, do tych łąk zielonych,
    Szeroko nad błękitnym Niemnem rozciągnionych;
    Do tych pól malowanych zbożem rozmaitem,
    Wyzłacanych pszenicą, posrebrzanych żytem;
    Gdzie bursztynowy świerzop, gryka jak śnieg biała,
    Gdzie panieńskim rumieńcem dzięcielina pała,
    A wszystko przepasane jakby wstęgą, miedzą
    Zieloną, na niej zrzadka ciche grusze siedzą.
</blockquote>
```

Dlatego myślę, że wiem już w jakim kontekście powinienem stosować
powyższe znaczniki. Ale zdaję sobie sprawę, że zanim w pełni zacznę
poprawnie stosować je to minie troszeczkę czasu.
