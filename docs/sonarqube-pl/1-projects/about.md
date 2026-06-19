# Koncepcja projektów

W SonarQube **projekt** jest centralną jednostką analizy jakości
kodu i bezpieczeństwa w platformie. Reprezentuje konkretną bazę kodu,
aplikację lub moduł, który chcesz analizować pod kątem problemów, takich
jak błędy, podatności, code smells i inne metryki jakości. Projekty w
SonarQube mogą być analizowane pojedynczo albo jako część większego
systemu, co pozwala precyzyjnie śledzić kondycję jednej aplikacji.

**Projekt** zwykle odpowiada pojedynczej aplikacji, usłudze
lub modułowi analizowanemu pod kątem jakości kodu. To kontener na
różne metryki, issue oraz ustawienia konfiguracyjne, których SonarQube
używa do śledzenia i oceny stanu bazy kodu.

## Klucz i nazwa projektu

- **Project Key**: unikalny identyfikator projektu.
- **Project Name**: czytelna nazwa wyświetlana w interfejsie.

## Analiza projektu

- **Bugs**: problemy mogące powodować błędy wykonania lub nieoczekiwane zachowanie.
- **Vulnerabilities**: potencjalne zagrożenia bezpieczeństwa, np. SQL injection albo XSS.
- **Code Smells**: problemy utrzymaniowe, które mogą nie być krytyczne,
  ale utrudniają zrozumienie lub utrzymanie kodu.

## Quality Gate

Każdy projekt może być powiązany z **Quality Gate**, czyli zestawem
warunków, które projekt musi spełnić, aby został uznany za "zdrowy".
Na przykład quality gate może wymagać braku krytycznych błędów
albo pokrycia testami powyżej określonego progu.

## Miary i trendy

- **Test Coverage**: procent kodu pokrytego testami automatycznymi.
- **Duplication**: procent zduplikowanego kodu w projekcie.
- **Ratings**: oceny niezawodności, bezpieczeństwa i utrzymywalności
  oparte na wykrytych issue.

## Dashboard projektu

Każdy projekt ma własny **dashboard**, który pokazuje widok wysokiego poziomu
wyników analizy, w tym kluczowe metryki, issue, trendy i status quality gate.

## Dostosowanie projektu

- **Rules**: określają, które reguły jakości i bezpieczeństwa stosować podczas analizy.
- **Notifications**: konfiguracja powiadomień dla zespołu o nowych issue
  albo niezaliczeniu quality gate.
- **Branch Analysis**: SonarQube wspiera analizę różnych gałęzi projektu,
  co pozwala śledzić jakość kodu na różnych etapach rozwoju.

## Projekty wielomodułowe

W przypadku większych aplikacji z wieloma komponentami SonarQube obsługuje
**projekty wielomodułowe**, gdzie każdy moduł jest traktowany jako podprojekt
w ramach projektu głównego. To szczególnie przydatne w architekturach
mikrousługowych lub aplikacjach monolitycznych z wyraźnie wydzielonymi modułami.

## Podsumowanie

Podsumowując, koncepcja **projektu** w SonarQube jest kluczowa dla
organizowania i śledzenia jakości kodu w czasie. Dzięki projektom zespoły
mogą analizować pojedyncze aplikacje, monitorować kluczowe metryki jakości,
egzekwować quality gates i priorytetyzować issue, aby utrzymywać kod zdrowy,
bezpieczny i łatwy w utrzymaniu.
