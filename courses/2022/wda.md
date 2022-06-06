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

1. (4 pkt.) wybór sortowania rosnącego bądź malejącego. Flaga 0 oznacza sortowanie rosnące, a 1 sortowanie malejące.
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
* Spróbuj zmierzyć rzeczywisty czas wykonania poszczególnych wersji sortowania - w tym celu wykorzystaj funkcje systemowe, std::chrono, std::clock lub znane z C time().

#### Kartkówka #2
Merge Sort: 
1. (4 pkt.) Zmodyfikuj implementację algorytmu Merge Sort o następującą funkcjonalność - zamiast dwóch podzadań `MERGESORT(A, p, s)` i `MERGESORT(A, s + 1, k)` występują cztery podzadania sortujące fragmenty tablicy o rozmiarze czterokrotnie mniejszym od wyjściowego.
2. (3 pkt.) Podaj równanie rekurencyjne zaimplementowanego algorytmu oraz oblicz jego złożoność obliczeniową (algorytm MST znajduje sie ponizej).
3. (1 pkt.) Jak różni się liczba porównań pomiędzy standardowym Merge Sort, a 4-way Merge Sort? (wykonaj kilka testów dla tablic różnej wielkości)

Proszę o przesłanie kodu źródłowego na maila piotr.kawa@pwr.edu.pl z tytułem "WDA - Lista 2".

<!-- ![Master Theorem](/assets/master_theorem.png) -->

#### Kartkówka #3

**Wybierz jedno z zadań**:
1. (8pkt) QuickSort:
  * Zaimplementuj procedurę `RANDOMIZED-QUICKSORT` tak by sortowała ona ciągi znaków. Sortowanie powinno wspierac dwa tryby - malejące i rosnące. Flaga 0 oznacza sortowanie rosnące, a 1 sortowanie malejące:
    * Sortowanie rosnące np. `['small', '42dog', 'dog', 'turtle', '1fluffy', 'corgi']` -> `['1fluffy', '42dog', 'corgi', 'dog', 'small', 'turtle']`
    * Sortowanie malejące np. `['small', '42dog', 'dog', 'turtle', '1fluffy', 'corgi']` -> `['turtle', 'small', 'dog', 'corgi', '42dog', '1fluffy']`

2. (8pkt.) Heap / HeapSort:
  * Zmodyfikuj procedurę `HeapSort3` tak by oparta o MinHeap, sortowała liczby naturalne w porządku malejącym.

Proszę o przesłanie kodu źródłowego na maila piotr.kawa@pwr.edu.pl z tytułem zawierającym numer wybranego zadania "WDA - Lista 3 (zad. 1/2)".


#### Kartkówka #4
Wykonaj następujące operacje na listach dwukierunkowych. Wyniki operacji `wypisz` załącz jako tekst w ramach wiadomości email zawierającej kod źródłowy zadania.


Uwaga:
* Indeksy w poleceniu numerowane są od 0 (np. pierwszy element to tablica[0], a trzeci element to tablica[2]),
* Jeśli nie jest powiedziane inaczej określenie `dodaj do listy` oznacza dodanie wartości na początek listy.


Zadanie:
* (4pkt) Zadanie 1: Wykonaj następujące operacje:
  1. stwórz listę,
  2. dodaj do listy wartości: [1,7,5,3,9]
  3. wypisz wartość długości listy
  4. usuń wartość 5 (jeśli implementacja opiera się na wskazaniu indeksu - podaj odpowiedni indeks)
  5. wstaw wartość 13 za wartością 7
  6. usuń element head
  7. usuń trzeci element
  8. wypisz długość listy
  9. wypisz zawartość listy
  10. wypisz wartość trzeciego elementu

* (4pkt) Zadanie 2: Wykonaj następujące operacje:
  1. stwórz listę A
  2. stwórz listę B
  3. dodaj do listy A wartości [7,6,2,1]
  4. dodaj do listy B wartości [3,4,5]
  5. wypisz wartości listy A i listy B
  6. odwróć listę B
  7. wstaw listę B na trzecim miejscu w liście A
  8. wypisz zawartość listy A
  9. połącz listę A i B (najpierw A, potem B)
  10. wypisz zawartość listy A
  11. wypisz wartość ósmego elementu listy A


Proszę o przesłanie kodu źródłowego na maila piotr.kawa@pwr.edu.pl z tytułem "WDA - Lista 4".
