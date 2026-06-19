# SAST (Static Application Security Testing)

**SAST (Static Application Security Testing)** to metoda analizy bezpieczeństwa
używana w SonarQube do identyfikacji podatności i błędów bezpieczeństwa
w kodzie źródłowym przed uruchomieniem aplikacji. SAST wykrywa potencjalne
ryzyka wcześnie w cyklu rozwoju, analizując kod pod kątem problemów takich
jak SQL injection, Cross-Site Scripting (XSS) czy niebezpieczna obsługa danych.

SonarQube integruje możliwości SAST, aby automatycznie skanować bazę kodu
i oznaczać issue, które mogłyby naruszać bezpieczeństwo aplikacji.
Dzięki SAST zespoły mogą adresować ryzyka już na etapie developmentu,
zmniejszając koszt i złożoność późniejszych napraw.

## Wykrywanie podatności bezpieczeństwa

- **SQL Injection**: niesprawdzone dane wejściowe mogą pozwolić atakującym
  manipulować zapytaniami do bazy.
- **Cross-Site Scripting (XSS)**: brak poprawnej sanityzacji danych wejściowych
  może umożliwić wstrzyknięcie złośliwych skryptów.
- **Hardcoded Secrets**: wykrywanie haseł, kluczy API i innych danych
  wrażliwych zapisanych na stałe w kodzie.

## Konfigurowalne reguły bezpieczeństwa

SonarQube udostępnia szeroki zestaw wbudowanych reguł bezpieczeństwa
wykrywających typowe podatności. Reguły te można dostosowywać do potrzeb
projektu lub organizacji.

## Integracja z pluginami bezpieczeństwa

Możliwości SAST w SonarQube często rozszerza się przez dodatkowe pluginy
bezpieczeństwa (np. **SonarQube Security Plugin** albo **SonarLint**),
które dostarczają bardziej zaawansowane kontrole i głębszą analizę kodu.

## Security Hotspots

SonarQube wprowadza pojęcie **Security Hotspots**, czyli potencjalnych
problemów bezpieczeństwa wymagających ręcznego przeglądu. To miejsca, gdzie
mogą istnieć podatności, ale narzędzie wymaga oceny człowieka, by określić
wagę i poprawność zgłoszenia. Pozwala to zespołom skupić się na krytycznych
obszarach kodu wymagających dokładniejszej analizy.

## Priorytetyzacja oparta na ryzyku

Issue bezpieczeństwa wykryte przez SAST są kategoryzowane i priorytetyzowane
według wagi (np. Blocker, Critical, Major). Dzięki temu zespoły mogą najpierw
adresować najistotniejsze zagrożenia.

## Skanowanie ciągłe

SonarQube stale analizuje kod podczas cykli integracyjnych, co oznacza, że
każdy commit i pull request może być automatycznie skanowany pod kątem
podatności bezpieczeństwa. To wspiera ciągłe wykrywanie i naprawę problemów
zamiast czekania na okresowe audyty.
