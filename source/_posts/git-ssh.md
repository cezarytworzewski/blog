----
title: Czym jest GIT? Klucze SSH - jak to zrozumieć?
----

Drugi post postanowiłem, że będzie poświęcony konfiguracji `GIT'a` krok po
kroku.
Sam wiele razy miałem sytuację, że posypały mi się `klucze SSH` w `GIT` lub wystepowały inne błędy.
Postanowiłem napisać wszystko kroku po kroku, bynajmniej mam taką nadzieję, żebym na przyszłośc nie musiał szukać,
męczyć się jak to skonfigurować. Wszystko będę miał w jednym miejscu. Mam również nadzieję, że spodoba Wam się mój wpis, mój blog i bdzie dla Was pożyteczny.

Myślę, że w ten sposób będę mógł usystematyzować swoją wiedzę.

#### W skrócie, czym jest `GIT`?
* to system kontroli wersji
* system kontroli wersji śledzi wszystkie zmiany jakie zostały dokonane
na pliku, plikach, bądź całym katalogu
* umożliwia przywrócenie wcześniejszej wersji projektu


#### Jak skonfigurować GIT'a z GitHubem?

1. Jesli nie posiadamy konta na `GitHub` musimy je założyć.
Tutaj założymy konto: <https://github.com/join?source=header-home>

    Jeśli posiadamy konto to wszystko jak na razie jest dobrze. :-)

2. Na komputerze lokalnym tworzę folder o nazwie np.:  `Pliki` oraz tworzę plik `index.html`
   dalej... muszę połączyć git'a lokalnie z kontem `GitHub` na serwerze:

* muszę utworzyć klucz SSH, wykonując polecenie: `ssh-keygen -t rsa -C "adres-email"`

* następnie, muszę przejść do katalogu użytkowniak `/.ssh`. Z poziomu terminala w Linux'ie do katalogu użytkownika przechodzimy za pomocą
polecenia `cd ~` - znak TYLDA. Są tam dwa pliki, interesuje mnie plik o nazwie: `id_rsa.pub` --> wchodzę do niego i kopiuję całą jego zawartość.

Zawartość pliku `id_rsa.pub` jest moim kluczem publiczny, którą to wklejam na koncie `GitHub w zakładce `Settings` --> `SSH and GPG keys`.

Następnie w konsoli wydaję polecenie:
	`git init`,
	`git add .` ( . - kropka oznacza, że chce dodać wszystkie pliki)
			Jeśli chciałbym dodać tylko jeden plik to wydam polecenie
			`git add index.html`, gdzie plik `index.html` jest moim
			plikiem, który chce wysłać na serwer


```
	git status (opcjonalnie)
	git commit -m "commit-message"
	git remote add origin git@github.com:NAZWA_UŻYTKOWNIKA_GITHUB/NAZWA_REPOZYTORIUM.git
	git push -u origin master
```


I pliki są już na [GiTHub](http://www.github.com).