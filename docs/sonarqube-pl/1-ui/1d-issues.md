# Issue i ich właściwości

W SonarQube **issue** to problemy wykryte podczas statycznej analizy kodu
projektu. Mogą obejmować błędy, podatności, code smells i inne zagadnienia
związane z utrzymywalnością. Issue są kategoryzowane według typu, wagi i
lokalizacji w kodzie, co ułatwia ich priorytetyzację i naprawę.

## 1. Bugs

- **Definicja**: bugs to problemy, które mogą prowadzić do błędów wykonania
  albo nieoczekiwanego zachowania aplikacji.
- **Wpływ**: bugs należy naprawiać szybko, bo często wpływają na funkcjonalność.
- **Waga**: bugs mogą być klasyfikowane jako Blocker, Critical, Major, Minor
  albo Info — zależnie od wpływu.

## 2. Vulnerabilities

- **Definicja**: vulnerabilities to problemy bezpieczeństwa, które mogą
  narażać aplikację na ataki, np. SQL injection, Cross-Site Scripting (XSS)
  albo nieprawidłową kontrolę dostępu.
- **Wpływ**: podatności mogą mieć poważne konsekwencje, w tym wycieki danych
  lub nieautoryzowany dostęp.
- **Waga**: podobnie jak bugs, są klasyfikowane jako Blocker, Critical, Major, Minor, Info.

## 3. Code Smells

- **Definicja**: code smells to problemy utrzymywalności, które nie muszą
  wpływać na działanie aplikacji, ale utrudniają zrozumienie i rozwój kodu.
- **Przykłady**: długie metody, duplikacja kodu, słabe nazwy zmiennych.
- **Wpływ**: code smells zwiększają dług techniczny i utrudniają utrzymanie
  projektu w dłuższej perspektywie.

## 4. Duplications

- **Definicja**: duplicated code to identyczne lub podobne fragmenty kodu
  powielone w wielu miejscach.
- **Wpływ**: duplikacja zwiększa złożoność utrzymania i ryzyko błędów, gdy
  zmiany trzeba wprowadzać we wszystkich kopiach.
- **Waga**: duplikacje zwykle nie są klasyfikowane wagą, ale są śledzone
  jako obszary wymagające refaktoryzacji.

## Właściwości issue

### 1. Severity

- **Blocker**: krytyczne problemy wymagające natychmiastowej reakcji.
- **Critical**: problemy o wysokiej wadze, które trzeba szybko rozwiązać.
- **Major**: ważne, ale nie natychmiast pilne.
- **Minor**: problemy o mniejszym wpływie, ale warte rozwiązania.
- **Info**: niskoprioritytowe kwestie, często kosmetyczne.

### 2. Type

- **Bug**: defekt, który może powodować błąd lub nieoczekiwane zachowanie.
- **Vulnerability**: problem bezpieczeństwa narażający projekt na ryzyko.
- **Code Smell**: problem utrzymywalności sugerujący słabe praktyki kodowania.
- **Duplicated Code**: powtórzony kod, który warto zrefaktoryzować.

### 3. Status

- **Open**: issue zostało wykryte, ale jeszcze nie rozwiązane.
- **Fixed**: issue zostało rozwiązane i nie występuje już w kodzie.
- **Won't Fix**: issue przejrzane i uznane za nieistotne lub nienaprawialne.
- **Reopened**: issue wcześniej zamknięte, które pojawiło się ponownie po zmianie kodu.

### 4. Assignee

Issue mogą być przypisywane do konkretnego dewelopera lub zespołu
odpowiedzialnego za ich naprawę.

### 5. Location

- **File**: plik, w którym wykryto issue.
- **Line Number**: konkretna linia, w której problem występuje.

### 6. Tags

Tagi pomagają kategoryzować issue i ułatwiają grupowanie oraz filtrowanie.
Przykładowe tagi: "security", "refactoring", "test".

---

## Ćwiczenia

### Ćwiczenie 1: Przegląd dashboardu Issues

**Cel:**  
Poznaj dashboard issues i sposób ich kategoryzowania.

**Zadania:**
1. Otwórz sekcję **Issues** w projekcie SonarQube.
2. Przefiltruj issue wg **severity** (Blocker, Critical, Major itd.).
3. Przejrzyj kilka issue i zanotuj ich **type**, **severity** i **status**.

---

### Ćwiczenie 2: Analiza i priorytetyzacja issue

**Cel:**  
Naucz się ustalać priorytety issue na podstawie wagi i wpływu.

**Zadania:**
1. Przejdź do sekcji **Issues** i odfiltruj issue typu **Blocker**.
2. Przejrzyj issue i zanotuj ich **location** oraz **type**.
3. Omów, jak postępować z najbardziej krytycznymi problemami.

---

### Ćwiczenie 3: Analiza code smells i duplikacji

**Cel:**  
Zrozum wpływ code smells i zduplikowanego kodu.

**Zadania:**
1. Przejdź do sekcji **Code Smells** i odfiltruj issue o wadze **Major**
   i **Minor**.
2. Przejrzyj sekcję **duplicated code** i wskaż obszary wymagające refaktoryzacji.
3. Zaproponuj sposoby poprawy utrzymywalności kodu przez redukcję
   zidentyfikowanych code smells i duplikacji.
