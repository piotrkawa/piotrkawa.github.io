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


## Aktualności
### 28.03.2022

#### Kartkówka #1
Rozszerz implementację algorytmu Insertion Sort o następujące funkcjonalności:

1. (4 pkt.) wybór sortowania rosnącego bądź malejącego. Flaga 0 oznacza sortowanie rosnące, a 1 sortowanie malejące,
2. (4 pkt.) wybór górnego zakresu liczb (x) na jakich operujemy (zakładamy, że sortowane wartości są losowe z przedziału [0, x]).

Obydwie opcje mają być przekazywane na standardowe wejście (np. w implementacji C++ korzystając z funkcji `std::cin`).

Proszę o przesłanie kodu źródłowego na maila piotr.kawa@pwr.edu.pl z tytułem "WDA - Lista 1".


![Master Theorem](/assets/master_theorem.png)
