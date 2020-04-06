---
title: Dlaczego nie można modyfikować pliku bootstrap.min.css?
date: 2018/06/15
---

Czym jest **Bootstrap**? Bootstrap jest to framework. Służy on do tworzenia
stron internetowych w sposób *responsywny*, czyli taki, gdzie strona będzie
się dostosowywać do każdego urządzenia, nie zależnie od wielkości przeglądarki.

Framework ten można pobrać lokalnie na swój komputer lub z serwera:

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css"/>
```

## Dlaczego nie powinniśmy go modyfikować

Chodzi oto, że Bootstrap posiada szereg _domyślnie_ stworzonych elementów,
które w sposób "automatyczny" dadzą nam wizualnie świetną stronę internetową.

Więc, posiada on edytowane już selektory, które możemy zostawić
i strona będzie nam się dobrze prezentować.

Jeśli chcemy zmodyfikować, to robimy to inaczej. Tworzymy _nowy_ plik
`style.css` i modyfikujemy dane selektory. Nadpisujemy je.

Wyobraź sobie, że Bootstrap posiada już stworzony selektor `h1`, którego
nie musimy edytować, ale jednak załóżmy, że chcemy zmienić `font-size` na
`30px`, gdzie domyślnie ta wartość wynosi przykładowo `18px`.

Ponadto, nie powinniśmy edytować tego pliku, ponieważ został on poddany
procesowi **minifikacji kodu**, o którym mówi mój kolega w swoim `vlog'u`:

<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/8Mhvn2jImwI"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
></iframe>

*Minifikacja kodu* jest to usunięcie w całym pliku białych znaków.

Plik, który został poddany minifikacji kodu, byłby - a dokładniej jest trudny
do edycji. Jest on nieczytelny, więc edycja go zajęła by nam "setki godzin".

Innym powodem według mnie dlaczego nie powinniśmy go edytować, to taka sytuacja
gdzie, tą bibliotekę, będziemy chcieli wykorzystać w innym projekcie i od nowa
musielibyśmy dostosowywać właściwości CSS naszej strony. Dlatego jak wspomniałem
wcześniej - najlepiej jak stworzymy drugi plik.

Albo jeśli edytujemy, to nie powinniśmy się łudzić, że zostanie ona update'owana
przez twórców Twitter'a. Musielibyśmy wprowadzić na prawdę bardzo dobre
*nowe* funkcjonalności we framework'u.

To się tyczy nie tylko Bootstrap'a, a także _innych_ framework'ów.
