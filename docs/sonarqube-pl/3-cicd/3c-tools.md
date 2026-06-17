# Import wyników analizy z narzędzi zewnętrznych

SonarQube umożliwia import wyników analizy z narzędzi zewnętrznych,
takich jak **Bandit**, **Pylint**, **Coverage** i **Mypy**.
Ta integracja rozszerza analizę SonarQube o wyniki wyspecjalizowanych
narzędzi do analizy statycznej i testów, które nie zawsze są natywnie
obsługiwane. Łącząc wyniki z wielu źródeł, można uzyskać pełniejszy obraz
jakości, bezpieczeństwa i zgodności projektu.

## 1. Integracja narzędzi zewnętrznych

SonarQube pozwala importować wyniki narzędzi zewnętrznych przez konfigurację
**SonarQube Scanner** i dodanie plików raportów generowanych np. przez
**Bandit**, **Pylint**, **Coverage** i **Mypy**. Narzędzia te analizują kod
i tworzą raporty, które SonarQube może sparsować, aby wzbogacić analizę.

## 2. Obsługiwane narzędzia zewnętrzne

Krótki przegląd narzędzi często integrowanych z SonarQube:

- **Bandit**: narzędzie statycznej analizy bezpieczeństwa dla Pythona.
  Wykrywa typowe problemy security; wyniki można importować do SonarQube.
- **Pylint**: analizator statyczny Pythona sprawdzający błędy, zgodność
  ze standardami i code smells. Wyniki można importować do SonarQube, by
  poszerzyć metryki jakości.
- **Coverage**: narzędzia pokrycia kodu (np. **coverage.py**) mierzą, jaka
  część kodu jest pokryta testami; wyniki można pokazać w SonarQube.
- **Mypy**: statyczny checker typów dla Pythona oparty na adnotacjach typów;
  wyniki można importować, aby wzmacniać bezpieczeństwo typów.

## 3. Import wyników do SonarQube

Aby importować wyniki narzędzi zewnętrznych, zwykle konfiguruje się plik
**sonar-project.properties**, wskazując lokalizacje raportów.

Przykłady:
- Dla **Pylint** użyj `sonar.python.pylint.reportPaths`.
- Dla **Coverage** użyj `sonar.python.coverage.reportPaths`.
- Dla **Bandit** użyj `sonar.python.bandit.reportPaths`.
- Dla **Mypy** użyj `sonar.python.mypy.reportPaths`.

## 4. Parsowanie i prezentacja wyników

Po skonfigurowaniu raportów i imporcie do SonarQube wyniki można przeglądać
w interfejsie SonarQube, m.in. w zakładkach **Issues** i **Coverage**,
obok natywnej analizy SonarQube.

---

## Ćwiczenia

### Ćwiczenie 1: Konfiguracja importu wyników Pylint

**Cel:**  
Naucz się integrować wyniki **Pylint** z SonarQube.

**Zadania:**
1. Uruchom analizę **Pylint** dla projektu Python i wygeneruj raport XML.
2. W pliku `sonar-project.properties` ustaw
   `sonar.python.pylint.reportPaths`, wskazując raport Pylint XML.
3. Uruchom SonarScanner i sprawdź, czy issue z **Pylint** pojawiają się
   na dashboardzie SonarQube.

---

### Ćwiczenie 2: Import wyników Coverage do SonarQube

**Cel:**  
Zintegruj wyniki **code coverage** z SonarQube.

**Zadania:**
1. Wygeneruj raport pokrycia za pomocą **coverage.py** lub innego narzędzia.
2. W pliku `sonar-project.properties` ustaw
   `sonar.python.coverage.reportPaths` na lokalizację raportu.
3. Uruchom SonarScanner i sprawdź zakładkę **Coverage** w SonarQube,
   aby potwierdzić, że metryki są widoczne.

---

### Ćwiczenie 3: Import wyników bezpieczeństwa Bandit

**Cel:**  
Zaimportuj wyniki analizy bezpieczeństwa **Bandit** do SonarQube.

**Zadania:**
1. Uruchom **Bandit** dla projektu Python i wygeneruj raport.
2. Dodaj ścieżkę do raportu Bandit w `sonar-project.properties`
   przez właściwość `sonar.python.bandit.reportPaths`.
3. Uruchom SonarScanner i sprawdź sekcję **Security** w SonarQube,
   aby zweryfikować wykryte podatności.
