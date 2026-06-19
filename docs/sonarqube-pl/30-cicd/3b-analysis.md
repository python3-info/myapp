# Analiza statyczna i Quality Gates

W SonarQube **analiza statyczna** to proces badania kodu źródłowego
projektu w celu wykrycia potencjalnych problemów, takich jak bugs,
vulnerabilities, code smells i inne kwestie jakości — bez uruchamiania
programu. Analiza opiera się na zdefiniowanych regułach i metrykach.
**Quality gates** to kluczowa funkcja utrzymania wysokiej jakości kodu,
ponieważ ustawia progi dla najważniejszych metryk. Jeśli kod nie spełni
wymagań quality gate, analiza może zakończyć się niepowodzeniem, blokując
merge lub wdrożenie słabego jakościowo kodu.

## 1. Analiza statyczna

Analiza statyczna w SonarQube bada kod źródłowy projektu bez jego uruchamiania.
Opiera się na:

- **Rules**: predefiniowanych kontrolach różnych problemów jakości, np. bugs,
  vulnerabilities i code smells.
- **Metrics**: miarach takich jak złożoność, duplikacja i test coverage.

SonarQube używa różnych analizatorów (np. dla Javy, JavaScriptu, C# itd.),
aby przeprowadzać analizę i generować raporty jakości kodu.
Wyniki są kategoryzowane jako:

- **Bugs**: defekty mogące powodować błędy.
- **Vulnerabilities**: potencjalne zagrożenia bezpieczeństwa.
- **Code Smells**: praktyki, które nie muszą być błędne, ale można je poprawić.
- **Duplications**: powielone fragmenty kodu wpływające na utrzymywalność.

## 2. Quality Gates

**Quality gate** to zestaw warunków, które projekt musi spełnić, aby został
uznany za gotowy do integracji lub wdrożenia. Pozwala egzekwować konkretne
reguły i metryki jakości. SonarQube udostępnia domyślną quality gate,
ale można tworzyć własne dopasowane do potrzeb projektu.

Typowe warunki quality gate:

- **Brak nowych issue typu critical lub blocker**: blokowanie wprowadzania
  krytycznych problemów.
- **Code coverage on new code**: wymagany poziom pokrycia testami dla nowego
  lub zmienionego kodu.
- **Maintainability**: utrzymanie rozsądnej złożoności i łatwości utrzymania.
- **Duplications**: limit procentu duplikacji kodu.

Jeśli projekt nie spełni warunków quality gate, analiza kończy się statusem
failed, a build w CI/CD zostaje oznaczony jako nieudany.

## 3. Domyślna Quality Gate

- Brak nowych issue critical.
- Brak nowych issue blocker.
- Coverage na nowym kodzie.
- Brak nowej duplikacji.

Warunki te zapewniają bazowy poziom jakości dla każdego analizowanego projektu.

## 4. Niestandardowe Quality Gates

Administratorzy mogą tworzyć własne quality gates z progami m.in. dla:

- **Bugs**: maksymalna dozwolona liczba błędów.
- **Vulnerabilities**: maksymalna liczba podatności.
- **Code Coverage**: minimalny wymagany poziom pokrycia na nowym kodzie.
- **Duplications**: maksymalna liczba/procent zduplikowanych linii.

Własne quality gates można dopasować do typu projektu i standardów organizacji.

## Ćwiczenia

### Ćwiczenie 1: Przegląd i modyfikacja domyślnego Quality Gate

## Cel 
 
Naucz się przeglądać i modyfikować domyślne ustawienia quality gate.

## Zadania

1. Przejdź do **Administration > Quality Gates** w SonarQube.
2. Przejrzyj domyślną quality gate i jej warunki.
3. Zmień warunki, np. zwiększ minimalne pokrycie testami albo
   zmodyfikuj dozwoloną liczbę błędów.
4. Zastosuj zmodyfikowaną quality gate do projektu.

# Utworzenie i przypisanie własnego Quality Gate

## Cel 
 
Poćwicz tworzenie i przypisywanie własnej quality gate do projektu.

## Zadania

1. Przejdź do **Administration > Quality Gates**.
2. Utwórz własną quality gate, definiując warunki dotyczące pokrycia
   nowego kodu, progów błędów i limitów duplikacji.
3. Przypisz ją do projektu.
4. Uruchom analizę i sprawdź, czy projekt przechodzi lub nie przechodzi
   zgodnie z warunkami.

# Analiza wyników i poprawa jakości kodu

## Cel 
 
Przeanalizuj wyniki analizy statycznej i napraw issue wskazane przez SonarQube.

## Zadania

1. Uruchom analizę statyczną dla przykładowego projektu.
2. Przejrzyj wyniki w zakładce **Issues** dla kategorii takich jak bugs,
   vulnerabilities i code smells.
3. Napraw zidentyfikowane problemy w kodzie.
4. Uruchom analizę ponownie i sprawdź, czy issue zostały rozwiązane oraz
   quality gate jest zaliczony.
