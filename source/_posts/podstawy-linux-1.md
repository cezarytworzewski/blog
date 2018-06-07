----
title: Nauka Linux'a od podstaw (1)
date: 2018/06/07
----

Jak wiecie, dodatkiem do mojej nauk `Front-end'u` jest nauka `Linux'a`. Fizycznie posiadam `Ubuntu` i na maszynie wirtualnej `CentOS`.

#### Podstawowe polcenie:
`pwd` - wskazuje bierzącą lokalizację (ścieżkę) w jakiej się znajdujemy
`cd ..` - zejście do katalogu wcześniej
`..cd..` - przechodzi dwa poziomy do tyłu
`clear` - czyści nam ekran
`whoami` - sprawdza nam, kto jest zalgowany aktualnie, jaki user

#### W czym może pomóc nam przycisk na klawiaturze `TAB`? 
Przycisk ten dopisuje na 'drugą' część polecenia! :)

### Co to ścieżka bezwzgledna?
To jest coś w stylu `pwd`. Przykład:
```
cd /home/cezary/Dokumenty/
```
Czyli jest to cała ścieżka dostępu.

#### Co to jest ścieżka względna?
W najprostszym dla mnie rozumieniu jest to przechodzenie stopniowe do katalogów, katalog po katalogu. Przykład poniżej:
```
cd home
cd cezary
cd Dokumenty
```

#### O nieee! Gdzie szukać pomocy? Nie działa mi to! 
Najpoluparniejszymi źródłami, z którego możemy czerpać wiedzę i możliwość rozwiązywania problemów jest:
* [Linux.pl](http://www.linux.pl)
* [Forum Linuxa](http://www.forum.linux.pl)

# PLIKI i KATALOGI

##### Najpopularnijesze polcenia to:
* `mkdir` - tworzy nam katalog. Przykład: `mkdir JavaScript`
* `rmdir` - usuwa nam plik lub pusty katalog
* `touch` - tworzy nam pliki wszelkiego typu. Pliki tekstowe, pliki `html`, `css` czy nawet pliki `js`. Możemy tworzyć kilka plików na raz -> `touch plik1.txt plik2.txt index.htmk`. Więcej do poczytania na [Jak stworzyć 3 pliki o różnych rozszerzeniach za pomocą 1 polecenia?](https://piecioshka.pl/blog/2018/05/21/jak-stworzyc-3-pliki-o-roznych-rozszerzeniach.html)
* `rm` - usunięcie pliku lib niepustego katalogu. Aby usunąć katalog wraz z zawartością wywołujmey polecenie `rm` z parametrem `r` --> `rm -r Dokumenty`.
* `cp` - kopiuje pliki lub katalogi w różne miejsca
*  `mv` - przeniesienie pliku lub katalogu (wycinanie). Zmienia też nazwę.

 
# KOPIOWANIE

#### Tworzę dwa foldery:
```
mkdir katalog1
mkdir katalog2
```
W `katalog1` tworzę dwa pliki: `touch plik1.txt plik2.txt`. `Katalog2` pozostaje pusty

* chce `plik1.txt` skopiować do `katalog2/`:
`cp katalog1/plik1.txt katalog2`
* chce `plik1.txt` skopiować do `katalog2/`, ale zmienić nazwę tego pliku:
`cp katalog1/plik1.txt katalog2/plik3.txt`
* chce skopiować całą zawartość `katalog1` do `katalog2/`:
`cp katalog1/* katalog2/`
* zmiana nazwy i przenoszenie 'czegoś' w inne miejsce:
`mv katalog1/plik1.txt katalog2/` - rezultat będzie taki, że `plik1.txt`zostanie przeniesiony (wycięty) z `katalog1` i będzie widoczny w `katalog2`
* chce zmienić nazwę pliku w tym samym katalogu:
```
cd katalog1/
mv plik1.txt nowaNazwaPliku.txt
```

# EDYTOR VIM

Edytor `VIM` posiada 3 tryby pracy:
* po wejściu do `VIM` np.: `vim plik1.txt` - wtedy mamy tryb normal
* jeśli kliknę literę `a` to będę wówczas w trybie input, czyli wprowadzanie, od tej chwili moge pisać w swoim edytorze
* żeby zapisać plik to:
  * najpierw klikam `ctrl + c`
  * znak `:` - czyli dwukropek uruchamia nam trzeci tryb, tzw. `tryb command-line`
  * żeby zapisać plik wciskam `w` (write)
  * żeby wyjść z pliku wciskam `:q` (quit)
  * albo od razu `:wq`

Aby wyświetlić całą zawartość pliku w terminalu wywołuję polecenie `cat`, `cat plik1.txt`.

#### Inne potrzebne polecenia w `VIM` to:
* `dd` - wycina nam daną linię, w której się ustawimy
* `p` - wkleja nam tekst pod tekstem, gdzie obecnie się znajdujemy kursorem
* `P` lub `Shift p` - wkleja nam tekst nad tekstem

#### Jak wyszukiwać dany tekst w `edytorze VIM`?

Jeśli chcemy wyszukać np. `pająk` tzn. słowo w tekście to robimy `/pająk`. Wyszukają nam się wyrazy o tej wartosci w całym naszym pliku.

#### Jak zmienić słowo w `VIM`?
Jesli chce zmienić wszystkie słowa`pająk` na `kot` to uruchamiam: `:%s/pająk/kot`

W kolejnych wpisach o Linuxie dowiem się jak instalować rzeczy. Oczywiście z pozionu `TERMINALA`

Zapraszam do czytania i komentwoania! :)



