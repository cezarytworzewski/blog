---
title: Jak łatwiej tworzyć artykuły na bloga z Hexo?
date: 2018-06-16
tags:
---

Odnalazłem nowy sposób na tworzenie artykułów  w oparciu o **Hexo**.

Do tej pory utrudniałem sobie pracę podczas tworzenia artykułów.
Tworzyłem nowy plik, pisałem artykuł a później dodawałem go z użyciem
programu `git`. Dodawanie artykułów trwało o wiele dłużej, gdyż musiałem
wydawać kolejno polecenia:

```bash
git add .
git commit -m "Initial post"
git push
hexo clean
hexo deploy
gh-pages -d public/
```

Teraz wystarczy, że wydam tylko 3 polecenia, które są opisanie poniżej. Na
szczęście udało mi się znaleźć sposób jak łatwiej dodać artykuł.

## 💡 Wskazówka

Ostatnie 3 polecenia możesz wykonać jednym:

```bash
npm run deploy
```

jeśli zdefiniujesz w pliku `package.json` nowe zadanie:

```json
"scripts": {
    "deploy": "hexo clean && hexo generate && gh-pages -d public/"
}
```

## Tworzenie artykułów (w aplikacji zbudowanej w oparciu o Hexo)

1. Jestem w katalogu projektu, moja ścieżka wygląda tak:

    ```text
    cezary:~/blog$
    ```

2. Teraz żeby dodać nowy artykuł muszę wydać w katalogu projektu polecenie:

    ```bash
    hexo new MOJ_NOWY_POST
    ```

    Stworzy mi się automatycznie plik o nazwie `MOJ-NOWY-POST.md`.
    Rozszerzenie `md` jest również dodawane automatycznie do pliku.

    Skąd wiem, że plik się poprawnie dodał? Otóż po wydaniu wcześniejszego
    polecenia otrzymam komunikat - informację o dodaniu poprawnie pliku.

    ```text
    INFO  Created: ~/blog/source/_posts/MOJ-NOWY-POST.md
    ```

3. Następnie edytuję plik `MOJ-NOWY-POST.md` dodając w nim treść artykułu.
    Zapisuję go i przechodzę dalej.

4. Wydam kolejno polecenia:

    ```bash
    hexo clean
    hexo generate
    gh-pages -d public/
    ```

<mark>Artykuł właśnie został dodany i opublikowany!</mark> 🚀

## Tworzenie artykułów roboczych (`draft`)

Możesz napisać kilka artykułów ale w wersji roboczej. Załóżmy, że napisałeś
artykuł, ale chcesz opublikować go jutro. Z Hexo masz taką możliwość.

Jak tworzyć artykuł w wersji roboczej:

* będąc w głównym katalogu mojego bloga wydaję polecenie:

    ```bash
    hexo new draft PLIK_ROBOCZY
    ```

    Informację o poprawnym dodaniu pliku roboczego znajdziesz poniżej:

    ```text
    INFO  Created: ~/blog/source/_drafts/PLIK-ROBOCZY.md
    ```

    Zapewne zauważyłeś, że w katalogu projektu, dodał się nowy folder o nazwie:

    ```text
    source/_drafts
    ```

* jeśli już edytowałeś swój plik roboczy, teraz pora żeby go opublikować

    ```bash
    hexo publish PLIK_ROBOCZY
    ```

    Potwierdzeniem poprawnego opublikowania jest otrzymanie komunikatu:
    
    ```text
    INFO  Published: ~/blog/source/_posts/PLIK-ROBOCZY.md
    ```

<mark>Twój szkic został zamieniony na artykuł!</mark> 🚀

_Wszystkie_ operacje musisz wykonywać będąc w _głównym_ katalogu projektu.

_Good luck!_
