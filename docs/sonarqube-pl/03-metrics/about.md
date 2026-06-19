# Metryki jakości

Metryki jakości w SonarQube dostarczają cennych informacji o kondycji
bazy kodu. Pozwalają deweloperom śledzić jakość, utrzymywalność i
bezpieczeństwo projektów w czasie. Pomagają wskazywać obszary do poprawy
i zapewniać zgodność kodu z wymaganymi standardami jakości.

## Bugs

- **Definicja**: bugs to problemy w kodzie, które mogą powodować błędy
  wykonania albo nieoczekiwane zachowanie.
- **Poziomy wagi**: bugs zwykle klasyfikuje się wg wagi
  (np. Blocker, Critical, Major, Minor). Błędy Blocker i Critical
  powinny być usuwane jako pierwsze, bo bezpośrednio wpływają na działanie
  aplikacji.

## Vulnerabilities

- **Definicja**: vulnerabilities to luki bezpieczeństwa, które potencjalnie
  mogą zostać wykorzystane przez atakujących.
- **Przykłady**: SQL injection, Cross-Site Scripting (XSS) i nieprawidłowe
  kontrole dostępu to częste podatności.
- **Poziomy wagi**: podobnie jak bugs, vulnerabilities są klasyfikowane
  jako Blocker, Critical, Major i Minor.

## Code Smells

- **Definicja**: code smells to problemy utrzymywalności, które nie zawsze
  powodują natychmiastowe błędy funkcjonalne, ale utrudniają zrozumienie,
  utrzymanie lub rozwój kodu.
- **Przykłady**: długie metody, zduplikowany kod i słabe nazewnictwo zmiennych.
- **Wpływ**: code smells nie wpływają bezpośrednio na funkcjonalność, ale
  mogą znacząco zwiększać koszt i czas utrzymania kodu w przyszłości.

## Duplications

- **Definicja**: duplicated code to fragmenty kodu powtarzające się
  w wielu miejscach.
- **Wpływ**: duplikacje utrudniają utrzymanie kodu i zwiększają ryzyko błędów,
  bo poprawka w jednym miejscu może nie zostać przeniesiona do wszystkich kopii.
- **Metryka**: duplikacje mierzy się jako procent bazy kodu, który się powtarza.

## Test Coverage

- **Definicja**: test coverage mierzy procent bazy kodu pokryty testami automatycznymi.
- **Cel**: wyższe pokrycie zwykle oznacza mniej nieprzetestowanych obszarów,
  co prowadzi do lepszej jakości i mniejszej liczby błędów.
- **Rekomendowany poziom**: często celem jest 80% pokrycia, ale właściwy
  próg zależy od potrzeb projektu.

## Security Rating

- **Definicja**: security rating mierzy ogólny poziom bezpieczeństwa projektu
  na podstawie liczby i wagi podatności.
- **Skala**: podobnie jak reliability, bezpieczeństwo jest oceniane od A (najlepiej) do E (najgorzej).
- **Cel**: wysoka ocena bezpieczeństwa oznacza mniej podatności i bezpieczniejszą aplikację.

## Reliability Rating

- **Definicja**: reliability rating mierzy ogólną niezawodność projektu
  na podstawie liczby i wagi błędów.
- **Skala**: niezawodność jest oceniana od A (najlepiej) do E (najgorzej).
- **Wpływ**: wysoka ocena niezawodności oznacza mniejsze ryzyko problemów wpływających na działanie systemu.

## Maintainability Rating

- **Definicja**: maintainability rating ocenia, jak łatwo utrzymywać i rozwijać bazę kodu projektu.
- **Skala**: także od A do E.
- **Czynniki**: ocena uwzględnia m.in. code smells, złożoność i duplikację kodu.
