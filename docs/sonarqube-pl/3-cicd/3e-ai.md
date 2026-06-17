# Integracja z narzędziami AI

SonarQube zaczęło integrować się z narzędziami opartymi o **AI**, aby
zwiększyć skuteczność wykrywania problemów jakości kodu, poprawić precyzję
analizy i dostarczać bardziej inteligentne sugestie dla deweloperów.
Takie integracje mogą ograniczać pracę ręczną i dostarczać wnioski wykraczające
poza tradycyjną analizę statyczną dzięki machine learningowi i AI.

Integracje AI mogą pomagać m.in. w wykrywaniu złożonych błędów i podatności
oraz w rekomendowaniu refaktoryzacji na podstawie wzorców poznanych z
dużych baz kodu. Dodanie AI do SonarQube wnosi dodatkową warstwę
inteligencji, która może poprawić jakość kodu na głębszym poziomie.

## 1. Sugestie reguł wspierane AI

SonarQube wykorzystuje AI do proponowania trafniejszych reguł na podstawie
wzorców obserwowanych w rzeczywistych bazach kodu. Pozwala to rekomendować
dodatkowe lub niestandardowe reguły jakości dopasowane do projektu.

## 2. Machine Learning do wykrywania błędów i podatności

AI może poprawiać wykrywanie **bugs** i **vulnerabilities** przez uczenie się
na historycznych wzorcach kodu. Modele AI mogą wskazywać problemy, których
trudniej szukać klasycznymi narzędziami analizy statycznej, skuteczniej
wyłapując zarówno oczywiste, jak i subtelne błędy.

## 3. Rekomendacje refaktoryzacji

Integracje AI mogą sugerować okazje do **refaktoryzacji** na podstawie
code smells, złożoności lub duplikacji. Modele analizują strukturę kodu
i proponują zmiany prowadzące do czystszego, łatwiejszego w utrzymaniu kodu.

## 4. Ciągłe uczenie na bazach kodu społeczności

Narzędzia AI zintegrowane z SonarQube mogą korzystać z ciągłego uczenia
na różnorodnych otwartoźródłowych bazach kodu i wkładzie społeczności.
Dzięki temu system rozwija się w czasie i odzwierciedla aktualne praktyki branżowe.

## 5. Lepsza redukcja false positives

AI może pomagać **redukować false positives** przez lepsze odróżnianie
realnych problemów od tych pozornych. Wykorzystując historię analiz i
ewoluujące wzorce kodu, system może precyzyjniej dostrajać wykrywanie.

---

## Ćwiczenia

### Ćwiczenie 1: Przegląd wykrywania code smells wspieranego AI

**Cel:**  
Zdobycie praktyki w wykrywaniu code smells z wykorzystaniem AI.

**Zadania:**
1. Przeanalizuj przykładowy projekt w SonarQube z włączonymi integracjami AI.
2. Przejrzyj zakładkę **Issues**, aby znaleźć code smells i sugestie poprawy.
3. Sprawdź, jak rekomendacje AI różnią się od klasycznej analizy statycznej,
   i wprowadź proponowane zmiany.

---

### Ćwiczenie 2: Test sugestii refaktoryzacji opartych o AI

**Cel:**  
Naucz się korzystać z sugestii refaktoryzacji generowanych przez AI.

**Zadania:**
1. Uruchom analizę SonarQube dla projektu ze znanymi problemami jakości
   (np. duplikacja kodu, wysoka złożoność).
2. Przejrzyj rekomendacje **refactoring** generowane przez AI.
3. Wdróż sugerowane zmiany i uruchom analizę ponownie, aby sprawdzić poprawę jakości.

---

### Ćwiczenie 3: Porównanie detekcji AI z klasyczną analizą statyczną

**Cel:**  
Porównaj wykrywanie issue przez AI i tradycyjną analizę statyczną.

**Zadania:**
1. Przeanalizuj projekt zarówno klasyczną analizą statyczną, jak i narzędziami AI
   (jeśli dostępne w Twojej konfiguracji SonarQube).
2. Porównaj wyniki obu metod i zanotuj różnice, szczególnie dla złożonych
   błędów i podatności.
3. Omów przewagi integracji AI nad standardową analizą statyczną oraz jej
   wpływ na proces wytwarzania oprogramowania.
