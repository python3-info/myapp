# Rules

W SonarQube **rules** definiują warunki i standardy kodowania, względem
których analizowany jest kod. Reguły służą do wykrywania potencjalnych
problemów w bazie kodu, takich jak bugs, vulnerabilities, code smells
i duplikacje. Pomagają utrzymać spójność i dobrą utrzymywalność kodu.

## 1. Reguły jakości kodu

Reguły te koncentrują się na dobrych praktykach kodowania i na tym, by kod
był czytelny, łatwy w utrzymaniu i wolny od zbędnego długu technicznego.

Przykład:
- Metoda nie powinna być zbyt długa (reguła długości metody).
- Zmienne powinny mieć znaczące nazwy (reguła konwencji nazewnictwa).

## 2. Reguły bezpieczeństwa

Reguły bezpieczeństwa pomagają wykrywać podatności, które mogłyby zostać
wykorzystane przez atakujących. Są kluczowe dla ochrony aplikacji i
zapobiegania incydentom bezpieczeństwa.

Przykład:
- Brak podatności SQL injection.
- Dane wejściowe muszą być sanitizowane, aby zapobiec XSS.

## 3. Reguły niezawodności

Reguły te mają zapewnić przewidywalne i poprawne działanie kodu podczas
wykonywania. Pomagają identyfikować potencjalne błędy i inne problemy
prowadzące do awarii w runtime.

Przykład:
- Unikaj dereferencji null pointer.
- Zapewnij poprawną obsługę wyjątków.

## 4. Reguły utrzymywalności

Reguły utrzymywalności zapewniają, że kod jest łatwy do utrzymania i
rozbudowy. Skupiają się na ograniczaniu złożoności, duplikacji i innych
czynników utrudniających przyszły rozwój.

Przykłady:
- Unikaj duplikacji kodu.
- Ogranicz rozmiar klas i metod.

## 5. Reguły wydajności

Reguły wydajności koncentrują się na optymalizacji kodu, aby działał
efektywnie. Pomagają wykrywać potencjalne wąskie gardła i nieefektywne
praktyki obniżające wydajność.

Przykłady:
- Unikanie nadmiernych alokacji pamięci.
- Używanie wydajnych algorytmów do typowych zadań.

## Właściwości reguł

### 1. Severity

- **Blocker**: krytyczne problemy wymagające natychmiastowej naprawy.
- **Critical**: problemy wysokiego priorytetu wymagające szybkiej reakcji.
- **Major**: istotne, ale niepilne problemy.
- **Minor**: problemy niskiego priorytetu.
- **Info**: niekrytyczne sugestie i usprawnienia.

### 2. Status

- **Active**: reguła jest stosowana podczas analizy kodu.
- **Inactive**: reguła nie jest obecnie stosowana (wyłączona lub zmieniona).
- **Deprecated**: reguła jest przestarzała i niezalecana.

### 3. Kategorie

- **Bug**
- **Vulnerability**
- **Code Smell**
- **Security**
- **Best Practices**

### 4. Tagi

Tagi służą do grupowania powiązanych reguł, co ułatwia filtrowanie i
zarządzanie nimi.
