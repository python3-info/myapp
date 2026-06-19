# Analiza statyczna i Quality Gates

W SonarQube **analiza statyczna** to proces badania kodu źródłowego
projektu w celu wykrycia potencjalnych problemów, takich jak bugs,
vulnerabilities, code smells i inne kwestie jakości — bez uruchamiania
programu. Analiza opiera się na zdefiniowanych regułach i metrykach.
**Quality gates** to kluczowa funkcja utrzymania wysokiej jakości kodu,
ponieważ ustawia progi dla najważniejszych metryk. Jeśli kod nie spełni
wymagań quality gate, analiza może zakończyć się niepowodzeniem, blokując
merge lub wdrożenie słabego jakościowo kodu.

## Analiza statyczna

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

## Quality Gates

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

## Domyślna Quality Gate

- Brak nowych issue critical.
- Brak nowych issue blocker.
- Coverage na nowym kodzie.
- Brak nowej duplikacji.

Warunki te zapewniają bazowy poziom jakości dla każdego analizowanego projektu.

## Niestandardowe Quality Gates

Administratorzy mogą tworzyć własne quality gates z progami m.in. dla:

- **Bugs**: maksymalna dozwolona liczba błędów.
- **Vulnerabilities**: maksymalna liczba podatności.
- **Code Coverage**: minimalny wymagany poziom pokrycia na nowym kodzie.
- **Duplications**: maksymalna liczba/procent zduplikowanych linii.

Własne quality gates można dopasować do typu projektu i standardów organizacji.
