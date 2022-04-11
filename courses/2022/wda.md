---
title: Wprowadzenie do algorytmiki
permalink: /teaching/wda-2022/
---

Prowadzone zajęcia:
* laboratoria - poniedziałek/TN, 15:15-16:55 @ A-1, s.250
* laboratoria - poniedziałek/TN, 17:05-18:45 @ A-1, s.249


## Zasady   
Kurs składa się z wykładu oraz laboratorium. Zasady zaliczenia kursu oraz listy zadań zostały zamieszczone na stronie wykładowcy, pod [tym linkiem](http://prac.im.pwr.wroc.pl/~zeberski/teaching/teaching.html). 

Laboratorium:
1. laboratorium służy uzupełnieniu i przećwiczeniu materiału przedstawionego na wykładzie
2. w czasie laboratorium rozwiązywane będą wybrane zadania z list przygotowanych przez wykładowcę, będą też udzielane wskazówki odnośnie rozwiązań pozostałych zadań - zarówno teoretycznych jak i implementacyjnych*
3. z każdą listą będzie powiązany termin jej oddania, wyrażony w numerze laboratoriów (nie są liczone laboratoria z pierwszego tygodnia, kiedy obie parzystości miały 45.minutowe zajęcia)
4. na zajęciach poprzedzających termin lub na stronie zostanie podana forma zaliczenia listy - możliwe jest krótkie zadanie implementacyjne, będące modyfikacją zadania z listy, zadanie teoretyczne pokazujące zrozumienie materiału w oparciu o zaimplementowane programy lub indywidualna prezentacja programów z listy wraz z omawianiem kodu oraz możliwymi drobnymi modyfikacjami
5. listy oceniane są na podstawie jakości rozwiązania (oraz jego prezentacji), jak i terminowości
6. za każdą listę zadań można uzyskać maksymalnie 8 punktów
7. za listę zadań zaliczoną ze spóźnieniem względem jej terminu można uzyskać: maksymalnie 4pkt, przy spóźnieniu nieprzekraczającym dwóch tygodni, 1 punkt przy spóźnieniu przekraczającym dwa tygodnie
8. dodatkowe punkty można otrzymać za prezentację własnych rozwiązań zadań teoretycznych; punkty z aktywności zostaną na koniec semestru doliczone do punktów z list - przelicznik konwersji zostanie ogłoszony wraz z ostatnią listą - zależnie od liczby opublikowanych zadań tego typu
9. wymóg obecności na laboratorium jest regulowany przez regulamin studiów oraz odpowiednie ZW
10. samodzielność: jeśli nie jest wyraźnie powiedziane inaczej, wszystkie rozwiązania muszą być samodzielne; rozwiązania niesamodzielne skutkują niezaliczeniem kursu bez względu na wcześniej zdobyte punkty.

___
## Aktualności
### 28.03.2022

#### Kartkówka #1
Rozszerz implementację algorytmu Insertion Sort o następujące funkcjonalności:

1. (4 pkt.) wybór sortowania rosnącego bądź malejącego. Flaga 0 oznacza sortowanie rosnące, a 1 sortowanie malejące,
2. (4 pkt.) wybór górnego zakresu liczb (x) na jakich operujemy (zakładamy, że sortowane wartości są losowe z przedziału [0, x]).

Obydwie opcje mają być przekazywane na standardowe wejście (np. w implementacji C++ korzystając z funkcji `std::cin`).

Proszę o przesłanie kodu źródłowego na maila piotr.kawa@pwr.edu.pl z tytułem "WDA - Lista 1".

### 11.04.2022

Zasady lista 3:
* Dane od użytkowników powinny być przyjmowane na standardowe wejście - poszczególne parametry wejściowe powinny być oddzielane białym znakiem (spacją lub enterem).
    * długośc tablicy do posortowania (n),
    * typ zmiennych do posortowania (T):
      * "int" - oznacza liczby całkowite,
      * "string" - oznacza zmienne będące ciągami alfanumerycznymi (tablice nie będą zawierać innych znaków),
      * "float" - liczby zmiennoprzecinkowe,
    * oddzielone spacją elementy tablicy,
    * dodatkowe dane (np. w zad. 8 - k).
* Na liście oceniany będzie zarówno HeapSort (zadania 7,8,9) jak i QuickSort (14,15,17).
* Dla każdego z algorytmów zliczaj liczbę porównań (elementów z tablicy do posortowania lub elementów pomocnicznych, nie uwzględniaj natomiast porównań iteratorów pętli itp.
* Dla każdego z algorytmów zlicz dodatkową pamięć niezbędną do przeprowadzenia algorytmu (a więc pomocnicze zmienne, pomocnicze kopie tablicy lub jej fragmentów, nie powinny być zliczane natomiast iteratory, zmienne dodatkowe wykorzystywane do zamienienia dwóch elementów miejscami etc. 
* Wynik działania programu powinien być przekazywany na standardowe wyjście - domyślnie powinny to być trzy zmienne oddzielone spacją: 
  * pierwsza określająca długość sortowanej tablicy,
  * druga - liczba wykonanych porównań,
  * trzecia - wymagana pamięć dodatkowa (jako jednostkę przyjmij rozmiar T lub bajty - skorzystaj np. z sizeof())
* Wszystkie dodatkowe informacje powinny być przekazywane na standardowe wyjście błędów - powinny to być przynajmniej dwie linie - w pierwszej oryginalna tablica, w drugiej posortowana tablica wynikowa, a w przypadku quick sorta również pozycja i wartość wybranego za każdym razem pivota



![Master Theorem](/assets/master_theorem.png)
