# Strona przeglądu projektu

**Project Overview Page** to centralny dashboard w SonarQube, gdzie
możesz uzyskać pełny obraz kondycji i jakości projektu. Zapewnia kluczowe
informacje o stanie bazy kodu, w tym ważne metryki, takie jak bugs,
vulnerabilities, code smells, test coverage itd.  
Ta strona pomaga deweloperom, liderom i menedżerom ocenić jakość kodu
i podejmować działania na podstawie wyników analizy.

## 1. Podsumowanie projektu

- **Project Name**: nazwa projektu.
- **Project Key**: unikalny identyfikator projektu.
- **Branch**: aktualnie analizowana gałąź (np. `main`, `develop`).
- **Last Analysis**: data i czas ostatniej analizy.

## 2. Kluczowe metryki

- **Bugs**: liczba wykrytych błędów.
- **Vulnerabilities**: liczba potencjalnych problemów bezpieczeństwa.
- **Code Smells**: liczba problemów utrzymywalności.
- **Duplications**: procent zduplikowanego kodu w projekcie.
- **Test Coverage**: procent kodu pokrytego testami jednostkowymi.
- **Reliability Rating**: ocena oparta na wadze błędów.
- **Security Rating**: ocena oparta na wadze podatności.
- **Maintainability Rating**: ocena utrzymywalności projektu.

## 3. Status Quality Gate

Pokazuje status **Quality Gate**, czyli zestawu warunków, które projekt
musi spełnić, aby został uznany za będący w dobrej kondycji. Na przykład
quality gate może wymagać braku krytycznych issue albo pokrycia testami
powyżej określonego progu.

## 4. Issue

- **New Issues**: issue wykryte w najnowszej analizie.
- **Fixed Issues**: issue, które zostały rozwiązane.
- **Open Issues**: issue nadal obecne w kodzie.

## 5. Miary i trendy

- **Measures**: szczegółowy widok metryk jakości projektu w czasie,
  np. liczby linii kodu, złożoności i duplikacji.
- **Trends**: wykresy pokazujące zmianę kluczowych metryk, np.
  pokrycia testami i ocen jakości, w czasie.

## 6. Ostatnia aktywność

Pokazuje ostatnie zmiany w projekcie, takie jak push kodu, wyniki
analizy czy rozwiązywanie issue.
