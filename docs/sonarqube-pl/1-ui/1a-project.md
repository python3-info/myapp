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

---

## Ćwiczenia

### Ćwiczenie 1: Nawigacja po liście projektów

**Cel:**  
Zapoznaj się z głównym dashboardem i jego funkcjami.

**Zadanie:**
1. Otwórz instancję SonarQube.
2. Przejrzyj **Project List Page**.
3. Dla każdego projektu znajdź i zanotuj:
   - **Project Name**
   - **Quality Gate Status** (np. Passed/Failed)
   - **Last Analysis Date**
4. Spróbuj sortować listę projektów po:
   - Last Analysis Date
   - Quality Gate Status

---

### Ćwiczenie 2: Zrozumienie statusu Quality Gate

**Cel:**  
Naucz się interpretować status quality gate dla projektów.

**Zadanie:**
1. Na **Project List Page** sprawdź kolumnę **Quality Gate Status**.
2. Zidentyfikuj projekty, które zaliczyły i nie zaliczyły quality gate.
3. Przefiltruj projekty tak, aby pokazać tylko te, które **nie zaliczyły** quality gate.
4. Zwróć uwagę na wzorce w projektach, które nie przechodzą quality gate.
   Czy wynika to z błędów, podatności czy code smells?

---

### Ćwiczenie 3: Przegląd metryk

**Cel:**  
Zrozum kluczowe metryki wyświetlane dla każdego projektu na głównym dashboardzie.

**Zadanie:**
1. Przejrzyj sekcję **Metrics** widoczną na **Project List Page**.
2. Dla co najmniej pięciu projektów zidentyfikuj:
   - **Code Smells**
   - **Bugs**
   - **Vulnerabilities**
3. Użyj **opcji filtrowania**, aby znaleźć projekty z najwyższym długiem technicznym,
   i zanotuj ogólne trendy w tych projektach.
4. Sprawdź, czy są projekty z **dużą liczbą code smells**
   lub **bugs**, i zanotuj ich wpływ na projekt.
