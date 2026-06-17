# Praca z false positives

W SonarQube **false positives** to issue błędnie oznaczone przez analizę.
Mogą wyglądać jak problemy w kodzie, ale nimi nie są — często z powodu
ograniczeń analizy statycznej albo specyfiki projektu. Poprawna obsługa
false positives jest ważna, żeby zespoły skupiały się na realnych
problemach zamiast na fałszywych alarmach.

## 1. Oznaczanie issue jako false positive

Gdy deweloper zidentyfikuje false positive, może oznaczyć issue w SonarQube.
To pomaga upewnić się, że problem nie będzie ponownie zgłaszany w kolejnych
analizach. Zwykle robi się to w sekcji **Issues**, wybierając opcję
**"False Positive"** dla danego zgłoszenia.

## 2. Wykluczanie issue

Jeśli konkretna reguła często generuje false positives, można ją
**wykluczyć** z analizy dla określonych plików, klas lub metod. Można to
zrobić przez **Quality Profiles**, gdzie reguły da się dezaktywować
albo wykluczać dla części bazy kodu. To trwalszy sposób rozwiązania
powtarzalnego problemu.

## 3. Dostosowanie reguł

Czasem false positives wynikają ze zbyt restrykcyjnych lub zbyt ogólnych
reguł. Wtedy pomocne jest **dostosowanie reguł** albo stworzenie własnych
quality profiles. Można zmienić parametry reguł, lepiej dopasować je do
projektu albo całkiem je wyłączyć.

## 4. Wyłączanie false positives komentarzami

SonarQube pozwala **dodawać komentarze** bezpośrednio w kodzie, aby
wykluczyć konkretne linie lub metody z analizy. Przykładowo można dodać
komentarz `//NOSONAR`, aby wyciszyć konkretny issue dla danej linii.
To przydatne, gdy chcemy zignorować false positive bez zmiany ustawień globalnych.

## 5. Tworzenie wyjątków dla false positives

W niektórych przypadkach issue oznaczone jako false positive mogą nadal być
istotne dla części projektów lub użytkowników. Przykładowo konkretne projekty
mogą mieć własne standardy kodowania albo decyzje architektoniczne
niezgodne z ogólnym zestawem reguł. SonarQube pozwala tworzyć **wyjątki**
dla projektów, co umożliwia lepsze dopasowanie analizy do potrzeb zespołu.

---

## Ćwiczenia

### Ćwiczenie 1: Oznaczenie issue jako false positive

**Cel:**  
Naucz się oznaczać issue jako false positive.

**Zadania:**
1. Przejdź do sekcji **Issues** projektu w SonarQube.
2. Wybierz issue, które uznajesz za false positive.
3. Oznacz je jako **False Positive** i upewnij się, że nie pojawia się
   ponownie w kolejnych skanach.

---

### Ćwiczenie 2: Wykluczenie reguły dla konkretnego pliku

**Cel:**  
Poćwicz wykluczanie reguły dla konkretnych plików lub fragmentów projektu.

**Zadania:**
1. Przejdź do sekcji **Quality Profiles** w **Administration**.
2. Zidentyfikuj regułę, która często generuje false positives.
3. Wyklucz tę regułę dla określonych plików lub klas.
4. Uruchom analizę i potwierdź, że reguła nie jest już stosowana
   dla wykluczonych plików.

---

### Ćwiczenie 3: Użycie komentarza suppressującego false positive

**Cel:**  
Naucz się używać komentarza `#NOSONAR`, aby wyciszyć konkretny issue.

**Zadania:**
1. W edytorze kodu znajdź linię, którą SonarQube oznacza jako false positive.
2. Dodaj na końcu linii komentarz `#NOSONAR`.
3. Uruchom nową analizę SonarQube i sprawdź, że issue zostało wyciszone
   dla tej konkretnej linii.
