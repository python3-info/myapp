# Clean as You Code

Koncepcja **Clean as You Code** w SonarQube zakłada usuwanie problemów
jakości kodu na bieżąco, w trakcie developmentu, zamiast odkładania ich
na później. Podejście to integruje ciągłą kontrolę jakości bezpośrednio
z workflow zespołu, dzięki czemu ogranicza narastanie długu technicznego
i pomaga utrzymać wysoki poziom jakości przez cały cykl życia projektu.

Korzystając z narzędzi takich jak SonarQube oraz stosując quality gates i
analizę statyczną na etapie developmentu, zespoły mogą dostarczać kod z
minimalną liczbą defektów i zgodny z dobrymi praktykami od samego początku.
To podejście promuje proaktywne rozwiązywanie problemów, ogranicza ryzyko
defektów i poprawia utrzymywalność w czasie.

## 1. Ciągłe kontrole jakości

SonarQube pomaga zespołom stale kontrolować jakość kodu przy każdym nowym
commicie, zwykle w pipeline **Continuous Integration (CI)**.
Gdy każdy commit uruchamia analizę, deweloperzy dostają szybki feedback
o nowych issue (bugs, vulnerabilities, code smells), dzięki czemu mogą
reagować od razu.

## 2. Quality Gates

W modelu **Clean as You Code** **quality gates** służą do egzekwowania
kryteriów, które nowy kod musi spełnić przed merge do gałęzi głównej.

Przykładowo:
- Brak nowych issue blocker i critical.
- Wystarczające pokrycie testami jednostkowymi.
- Brak nowej duplikacji kodu.

Quality gates zapobiegają wprowadzaniu nowych problemów i przepuszczają
dalej tylko kod o wymaganej jakości.

## 3. Natychmiastowy feedback

Koncepcja mocno opiera się na **natychmiastowym feedbacku** dla
deweloperów dzięki integracji SonarQube z CI, np. Jenkins, GitLab CI
czy GitHub Actions. Dzięki temu problemy są wykrywane i korygowane
zanim trafią do finalnego produktu.

## 4. Analiza przyrostowa

Zamiast analizować całą bazę kodu za każdym razem, SonarQube wykonuje
**analizę przyrostową** dla zmienionego kodu. Pozwala to skupić się
na nowo wprowadzonych issue bez ponownego przeglądu całego projektu.

## Ćwiczenia

### Ćwiczenie 1: Ustawienie Quality Gate dla nowego kodu

## Cel 
 
Naucz się konfigurować i stosować quality gates dla clean code.

## Zadania

1. Przejdź do **Administration > Quality Gates** w SonarQube.
2. Utwórz quality gate wymagający **braku nowych issue krytycznych**
   oraz **minimalnego code coverage**.
3. Przypisz quality gate do projektu.
4. Przetestuj bramkę, commitując kod z potencjalnymi problemami, i sprawdź,
   czy gate blokuje merge.

# Integracja SonarQube z pipeline CI/CD

## Cel 
 
Poćwicz integrację SonarQube z pipeline CI/CD, aby sprawdzać jakość przy każdym commicie.

## Zadania

1. Dodaj **analizę SonarQube** do pipeline CI
   (np. Jenkins, GitHub Actions lub GitLab CI).
2. Skonfiguruj pipeline tak, by uruchamiał SonarQube przy każdym commicie
   i raportował issue na bieżąco.
3. Zacommituj nowy kod i sprawdź, czy pipeline wykrywa problemy
   i blokuje merge, gdy quality gate nie przejdzie.

# Przegląd i naprawa issue na podstawie feedbacku SonarQube

## Cel 
 
Naucz się szybko przeglądać feedback SonarQube i od razu naprawiać problemy.

## Zadania

1. Uruchom **analizę SonarQube** dla projektu.
2. Przejrzyj zakładkę **Issues** pod kątem nowych bugs, vulnerabilities
   i code smells.
3. Napraw wskazane problemy w kodzie i uruchom analizę ponownie, aby
   potwierdzić, że zostały rozwiązane.
