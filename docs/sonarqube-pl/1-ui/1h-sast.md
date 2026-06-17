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

## 1. Wykrywanie podatności bezpieczeństwa

- **SQL Injection**: niesprawdzone dane wejściowe mogą pozwolić atakującym
  manipulować zapytaniami do bazy.
- **Cross-Site Scripting (XSS)**: brak poprawnej sanityzacji danych wejściowych
  może umożliwić wstrzyknięcie złośliwych skryptów.
- **Hardcoded Secrets**: wykrywanie haseł, kluczy API i innych danych
  wrażliwych zapisanych na stałe w kodzie.

## 2. Konfigurowalne reguły bezpieczeństwa

SonarQube udostępnia szeroki zestaw wbudowanych reguł bezpieczeństwa
wykrywających typowe podatności. Reguły te można dostosowywać do potrzeb
projektu lub organizacji.

## 3. Integracja z pluginami bezpieczeństwa

Możliwości SAST w SonarQube często rozszerza się przez dodatkowe pluginy
bezpieczeństwa (np. **SonarQube Security Plugin** albo **SonarLint**),
które dostarczają bardziej zaawansowane kontrole i głębszą analizę kodu.

## 4. Security Hotspots

SonarQube wprowadza pojęcie **Security Hotspots**, czyli potencjalnych
problemów bezpieczeństwa wymagających ręcznego przeglądu. To miejsca, gdzie
mogą istnieć podatności, ale narzędzie wymaga oceny człowieka, by określić
wagę i poprawność zgłoszenia. Pozwala to zespołom skupić się na krytycznych
obszarach kodu wymagających dokładniejszej analizy.

## 5. Priorytetyzacja oparta na ryzyku

Issue bezpieczeństwa wykryte przez SAST są kategoryzowane i priorytetyzowane
według wagi (np. Blocker, Critical, Major). Dzięki temu zespoły mogą najpierw
adresować najistotniejsze zagrożenia.

## 6. Skanowanie ciągłe

SonarQube stale analizuje kod podczas cykli integracyjnych, co oznacza, że
każdy commit i pull request może być automatycznie skanowany pod kątem
podatności bezpieczeństwa. To wspiera ciągłe wykrywanie i naprawę problemów
zamiast czekania na okresowe audyty.

---

## Ćwiczenia

### Ćwiczenie 1: Przegląd podatności bezpieczeństwa

**Cel:**  
Naucz się identyfikować podatności w kodzie przy użyciu SonarQube.

**Zadania:**
1. Przejdź do sekcji **Issues** w projekcie SonarQube.
2. Filtruj i wyszukuj issue związane z **security** (SQL Injection, XSS itd.).
3. Przejrzyj i skategoryzuj issue bezpieczeństwa według severity.

---

### Ćwiczenie 2: Analiza Security Hotspots

**Cel:**  
Naucz się identyfikować i przeglądać **Security Hotspots** w projekcie.

**Zadania:**
1. Przejdź do sekcji **Security Hotspots** w dashboardzie SonarQube.
2. Zidentyfikuj sekcje kodu oznaczone jako hotspots.
3. Zweryfikuj je i oznacz, czy to realne problemy, czy wymagają dalszych działań.

---

### Ćwiczenie 3: Dostosowanie reguł bezpieczeństwa

**Cel:**  
Dostosuj reguły bezpieczeństwa SonarQube do potrzeb projektu.

**Zadania:**
1. Przejdź do **Quality Profiles** w sekcji **Administration**.
2. Znajdź reguły bezpieczeństwa i zmodyfikuj jedną z nich
   (np. wyłącz lub skonfiguruj zgodnie z potrzebami projektu).
3. Zastosuj zaktualizowany zestaw reguł do projektu i uruchom nową analizę,
   aby sprawdzić wpływ na wyniki skanowania bezpieczeństwa.
