---
title: Nauka Linux'a od podstaw (2)
date: 2018/06/08
---

W tym artykule opiszę to czego się nauczyłem, czyli:
**instalacja oprogramowania**, **dowiązania w Linux**, **mechanizm CRON**

Warto wspomnieć, że instalować paczki **rpm** może jedynie użytkownik z
uprawnieniami **roota**!

## Instalacja oprogramowania

Na podstawie systemu CentOS do instalacji oprogramowania służą nam dwa
narzędzia:

* narzędzia automatyczne: **yum**
* narzędzia do paczek: **rpm**

Instalacja z paczki wygląda następująco:

* musimy pobrać odpowiednią paczkę, która jest zgodna z naszą architekturą OS
* wydajemy polecenie:
    +`rpm -i teamviewer_linux.rpm` albo lepszym rozwiązaniem będzie:
        -`rpm -Uvh teamviewer_linux.rpm` => gdzie poszczególne parametry
            oznaczają:
            +`U` - jest to inaczej polecenie `install` ale dodatkowo
                robi nam `update` naszej paczki
            +`v` - wyświetla nam informacje co aktualnie się wykonuje
                podczas instalacji
            +`h` - wyświetla nam procentoway pasek postępu

**Instalacja z narzędziem autoomatycznym:**
`yum install cups` - gdzie **cups** jest to serwer wydruku

## Dowiązania w Linux'ie

1. Wyróżniamy dwa `dowiązania` w Linux:

* **symboliczne**
* **twarde**

### Dowiązanie symboliczne

* przechodzę do katalogu domowego:

    ```bash
    cd ~
    ```

* tworzę folder i przechodzę do niego:

    ```bash
    mkdir linki
    cd linki/
    ```

* utworzę sobie plik tekstowy:

    ```bash
    vim plik.txt
    ```

    uzupełniam go zawartością po czym zapisuję. Więcej o edytorze VIM
    znajdziesz [tutaj](https://www.cezarytworzewski.github.io/blog/2018/06/07/podstawy-linux-1/)

* sprawdzam zawartość `plik.txt`:

    ```bash
    cat plik.txt
    ```

* teraz chce utworzyć **skrót** do pliku o nazwie **plik.txt**:

    Tworzę folder **dowiązania** w lokalizacji **tmp**:

    ```bash
        mkdir /tmp/dowiazania/
        cd /tmp/dowiazania/
    ```

* teraz tworzę dowiązanie do pliku:

    ```bash
        ln -s plik.txt /tmp/dowiazania/
    ```

    Parametr **s** oznacza, że symboliczne.

* przechodzę do katalogu **dowiazania**:

    ```text
      cd /tmp/dowiazania/
      ls //wyświetlam zawartość folderu **dowiazania**
      ls -l
    ```

### Dowiązania twarde

Jestem w katalogu **linki/**

```bash
ln bashplik.txt plik2.txt
```

Jeśli w poleceniu `ln` nie damy parametru to zostanie utworzone
dowiązanie twarde

Wyświetlimy sobie katalog:

```bash
cd /linki
ls
ls -l
```

Parametr `-l` wyświetla wszystko - uprawnienia, data,
godzina, user. Pierwsza kolumna oznacza uprawnienia do pliku,
natomiast druga to cyfra np: **1**, z każdym dowiązaniem twardym
liczba będzie rosnąć.

### Uwaga na dowiązania

* **dowiązanie symboliczne** mogę tworzyć na innych partycjach
* Natomiast **dowiązania twarde** musi znajdować się na partycji, w którym
    znajduje się oryginalny plik

### Mechanizm CRON

**Mechanizm CRON** jest to odpowiednik **Menadżera zadań** w **Windows**.
Możemy zdefiniować jakieś zadanie. Zakładam, że nie ma nas przy komputerze
a coś musi się wykonać np. jakaś aktualizacja systemu, albo tworzenie
automatycznych logów w systemie.

Mechanizm CRON posiada **7 pozycji:**:

```text
* * * * * root touch /tmp/plik.txt
```

### Opis wiersz z definicją zadania w CRON

| **Pozycja** | **Odpowiednik** |
|:-----------:|:---------------:|
|1            | minuta          |
|2            | godzina         |
|3            | miesiąc         |
|4            | dzień miesiąca  |
|5            | dzień tygodnia     |
|6            | użytkownik          |
|7            | zadanie do wykonania |

Mechanizmu CRON używa się do uruchamiania zadań (programów, komend,
skryptów) o konkretnej godzinie, dniu.
