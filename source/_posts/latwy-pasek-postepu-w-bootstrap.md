---
title: Tworzenie łatwego paska postępu w Bootstrap
date: 2018-07-01 17:01:18
tags:
---

Ostatnio uczę się intensywnie `Bootstrapa`.

Pominąłem opisanie jak stworzyć fajny przycisk w Bootstrap za pomocą klasy `.btn`.
Dość ciekawą rzeczą jest stworzenie prostego paska postępu, który można
zastosować podczas tworzenia strony, coś co określam terminem `strona w budowie`.

## Jak to wygląda

Pasek postępu wygląda następująco:

![imgur](https://image.ibb.co/eLjjNJ/pasek_post_pu.png)

## Jak to zrobić

1. Tworzymy sobie klasę główną dla naszego paska. Musimy stworzyć klasę
    zewnętrzną, która będzie przechowywać nasz pasek postępu:

    ```html
    <div class="progress">
    </div>
    ```

    To właśnie w powyższym kodzie określimy jak będzie wyglądał nasz pasek.

2. Teraz musimy stworzyć - do stworzenia paska służy prosta klasa Bootstrap'a
    o nazwie `progress-bar`. Kod wygląda następująco:

    ```html
    <div class="progress">
        <div class="progress-bar bg-success w-75">75%</div>
    </div>
    ```

    Efekt od strony Front-end'u wygląda tak:

    ![imgur](https://image.ibb.co/d2oppy/pasek_post_pu_2.png)

    Podstawowa klasa `progress-bar` tworzy pasek postępu koloru szarego,
    kolor ten jest widoczny po prawej stronie powyższego obrazka. Pasek postępu
    jest koloru zielonego - nie jest to domyślna wartość. Jest zielony ponieważ
    dodałem również klasę o nazwie `bg-success`, czyli tło zielone `bg` - to
    inaczej `background-color` określana jako właściwość w CSS. Warto również
    wspomnieć o kolejnej klasie jakiej użyłem, czyli klasa `w-75`. W
    Bootstrap'ie jest coś takiego jak **rozmiar okna**.

    Są dwa parametry odpowiadające za rozmiar:
         w - x (`w` - szerokość; `x` - wartość liczbowa)
         h - x (`h` - wysokość; `x` - wartość liczbowa)

    Wyróżniamy następujące wartości liczbowe: **25, 50, 75, 100**.
    Wartości te są wyrażone w procentach i jest ich tylko cztery.

    Na przykład wartość:

    `h-25` - określa wysokość na 25% wartości danego okna.
    `w-75` - określa szerokość okna o wartości 75% danego okna.

    W moim przypadku, chciałem nadać tło na 75% danego okna, czyli okna
    `progress-bar`.

3. Kolejna klasa warta uwagi to `progress-bar-striped`. Nadaje ona wzorek z
    pasków, u mnie będzie to kolor naprzemienny, raz jasnozielony a raz ciemnozielony.

    Wygląda to tak:
    ![Pasek progress-bar-striped](https://image.ibb.co/ftz7bd/pasek_post_pu_wzorek.png)

4. Ostatnią najfajniejszą według mnie jest klasa `progress-bar-animated`.
    Tworzy ona niemal identyczny pasek jak w klasie `progress-bar-striped`, z
    tym, że pasek jest ruchomy. Posiada on efekt przesuwania się paska od prawej
    do lewej strony.

    ```html
    <div class="progress">
        <div class="progress-bar bg-success w-75 progress-bar-striped progress-bar-animated">
        </div>
    </div>
    ```

    Żeby działał klasa `progress-bar-animated` musi być najpierw zdefiniowana
    klasa `progress-bar-striped`.

Nie jestem ekspertem w Bootstrap (mam nadzieję, że jeszcze), ale podoba mi
się możliwość tworzenia w nim stron internetowych. Podstawą na pewno jest dla
mnie, że konieczne jest zrozumienie `Grida` jak to jest z tymi kolumnami.
Reszta to już zapamiętanie kilku klas, dzięki którym możemy zrobić ciekawą
design.
