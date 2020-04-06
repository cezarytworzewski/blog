---
title: Czym jest Git? Klucze SSH - jak to zrozumieć?
date: 2018/05/31
update: 2018/06/01
---

Drugi post postanowiłem, że będzie poświęcony konfiguracji `Git'a` krok
po kroku.

Sam wiele razy miałem sytuację, że posypały mi się `klucze SSH` w `Git`
lub występowały inne błędy. Postanowiłem napisać wszystko kroku po kroku,
bynajmniej mam taką nadzieję, żebym na przyszłość nie musiał szukać,
męczyć się jak to skonfigurować. Wszystko będę miał w jednym miejscu.
Mam również nadzieję, że spodoba Wam się mój wpis, mój blog i będzie dla
Was pożyteczny.

Myślę, że w ten sposób będę mógł usystematyzować swoją wiedzę.

## W skrócie, czym jest `Git`?

* to system kontroli wersji
* system kontroli wersji śledzi wszystkie zmiany jakie zostały dokonane
    na pliku, plikach, bądź całym katalogu
* umożliwia przywrócenie wcześniejszej wersji projektu

## Jak skonfigurować Git'a z GitHub'em?

1. Jeśli nie posiadamy konta na `GitHub` musimy je założyć.
   Tutaj założymy konto: <https://github.com/join?source=header-home>

    Jeśli posiadamy konto to wszystko jak na razie jest dobrze. :-)

2. Na komputerze lokalnym tworzę folder o nazwie np.: `Pliki` oraz tworzę
    plik `index.html` dalej... muszę połączyć `git`-a lokalnie z kontem
    `GitHub` na serwerze:

* tworzę parę kluczy SSH (publiczny i prywatny), wykonując polecenie:

    ```text
        ssh-keygen -t rsa -C "adres-email"
    ```

* następnie, muszę przejść do katalogu użytkownika `~/.ssh`.

    Z poziomu terminala do katalogu użytkownika przechodzimy za pomocą
    polecenia `cd ~` - znak TYLDA. Są tam dwa pliki, interesuje mnie
    plik o nazwie: `id_rsa.pub` --> wchodzę do niego i kopiuję całą jego
    zawartość.

    Zawartość pliku `id_rsa.pub` jest moim kluczem publiczny, którą to
    wklejam na koncie `GitHub` w zakładce `Settings` --> `SSH and GPG keys`.

* następnie w konsoli wydaję polecenie:

    ```text
        git init
        git add .
    ```

    znak `.` - kropka oznacza, że chce dodać wszystkie pliki. Jeśli chciałbym
    dodać tylko jeden plik to wydam polecenie: `git add index.html`, gdzie
    plik `index.html` jest moim plikiem, który chce wysłać na serwer.

    ```bash
        git status (opcjonalnie)
        git commit -m "commit-message"
        git remote add origin git@github.com:NAZWA_UŻYTKOWNIKA_GITHUB/NAZWA_REPOZYTORIUM.git
        git push -u origin master
    ```

Pliki powinny być już dostępne w projekcie na [GitHub](http://www.github.com).
