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

```text
    git add .
    git commit -m "Initial post"
    git push
    hexo clean
    hexo deploy
    npm run deploy
```

teraz wystarczy, że wydam tylko 3 polecenia, które są opisanie poniżej. Na
szczęście udało mi się znaleźć  sposób jak łatwiej dodać artykuł.

## Tworzenie artykułów na Hexo

1) Jestem w katalogu projektu, moja ścieżka wygląda tak:

   `cezary:~/blog$`

2) Teraz żeby dodać nowy artykuł muszę wydać w katalogu projektu polecenie:

    `hexo new nowy-pliku`
   
    Stworzy mi się automatycznie plik o nazwie `nowy-plik.md`. Rozszerzenie `md`
    jest również dodawane automatycznie do pliku.
    
    Skąd wiem, że plik się poprawnie dodał? Otóż po wydaniu wcześniejszego
    polecenia otrzymam komunikat - informację o dodaniu poprawnie pliku.
    
        `INFO  Created: ~/blog/source/_posts/nowy-plik.md`      
3) Teraz wystarczy, że przejdę do mojego pliku `nowy-plik.md`. Tzn. otworzę go
    abym mógł go swobodnie edytować w celu napisania artykułu. Zapisuję go i
    przechodzę dalej.
4) Wydam kolejno polecenia:

    ```text
    hexo clean
    hexo deploy
    npm run deploy
    ```
    
Artykuł właśnie został dodany:)

## Tworzenie artykułów roboczych

Możesz napisać kilka artykułów ale w wersji roboczej. Załóżmy, że napisałeś
artykuł, ale chcesz opublikować go jutro. Z Hexo masz taką możliwość.

Jak tworzyć artykuł w wersji roboczej:

* będąc w głównym katalogu mojego bloga, czyli tutaj: `cezary:~/blog$`,
   wydaję polecenie: `hexo new draft plik-roboczy`
    
    Informację o poprawnym dodaniu pliku roboczego znajdziesz poniżej:
        
      `INFO  Created: ~/blog/source/_drafts/plik-roboczy.md`
        
     Za pewne zauważyłeś, że w katalogu projektu, dodał się nowy folder o nazwie:
        `_draft`

* jeśli już edytowałeś swój plik roboczy, teraz pora żeby go opublikować  na
    blogu.

    Wystarczy, że wydasz polecenie: `hexo publish plik-roboczy`
    
    I twój artykuł został dodany i posiada status opublikowany.
    
    Potwierdzeniem jest otrzymanie komunikatu: `INFO  Published: ~/blog/source/_posts/roboczy.md`

Wszystkie operacje musisz wykonywać będąc w głównym katalogu projektu.

_Good luck!_
