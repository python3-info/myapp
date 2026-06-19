# Import wyników analizy z narzędzi zewnętrznych

SonarQube umożliwia import wyników analizy z narzędzi zewnętrznych,
takich jak **Bandit**, **Pylint**, **Coverage** i **Mypy**.
Ta integracja rozszerza analizę SonarQube o wyniki wyspecjalizowanych
narzędzi do analizy statycznej i testów, które nie zawsze są natywnie
obsługiwane. Łącząc wyniki z wielu źródeł, można uzyskać pełniejszy obraz
jakości, bezpieczeństwa i zgodności projektu.

## Integracja narzędzi zewnętrznych

SonarQube pozwala importować wyniki narzędzi zewnętrznych przez konfigurację
**SonarQube Scanner** i dodanie plików raportów generowanych np. przez
**Bandit**, **Pylint**, **Coverage** i **Mypy**. Narzędzia te analizują kod
i tworzą raporty, które SonarQube może sparsować, aby wzbogacić analizę.

## Obsługiwane narzędzia zewnętrzne

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

## Import wyników do SonarQube

Aby importować wyniki narzędzi zewnętrznych, zwykle konfiguruje się plik
**sonar-project.properties**, wskazując lokalizacje raportów.

Przykłady:
- Dla **Pylint** użyj `sonar.python.pylint.reportPaths`.
- Dla **Coverage** użyj `sonar.python.coverage.reportPaths`.
- Dla **Bandit** użyj `sonar.python.bandit.reportPaths`.
- Dla **Mypy** użyj `sonar.python.mypy.reportPaths`.

## Parsowanie i prezentacja wyników

Po skonfigurowaniu raportów i imporcie do SonarQube wyniki można przeglądać
w interfejsie SonarQube, m.in. w zakładkach **Issues** i **Coverage**,
obok natywnej analizy SonarQube.
