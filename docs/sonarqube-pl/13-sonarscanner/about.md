# SonarScanner i jego konfiguracja

**SonarScanner** to narzędzie wiersza poleceń używane do analizy kodu
źródłowego projektu i wysyłania wyników do serwera SonarQube. To podstawowy
mechanizm analizy projektu w procesach Continuous Integration (CI) oraz
podczas lokalnych buildów. SonarScanner najczęściej integruje się z
narzędziami buildowymi takimi jak Maven, Gradle albo uruchamia bezpośrednio
z CLI.

## 1. Czym jest SonarScanner?

SonarScanner to oficjalny skaner służący do wysyłania wyników analizy do
instancji SonarQube. Odczytuje kod źródłowy, stosuje reguły jakości i
raportuje bugs, vulnerabilities, code smells i inne metryki jakości.
Może być używany dla różnych technologii, m.in. Java, C#, Python,
JavaScript i wielu innych.

## 2. Typy SonarScannera

- **SonarScanner for Maven**: integracja dla projektów Maven;
  uruchamia analizę w cyklu życia Mavena.
- **SonarScanner for Gradle**: analogiczna integracja dla projektów Gradle.
- **SonarScanner CLI**: samodzielna wersja uruchamiana ręcznie z linii poleceń.

## 3. Konfiguracja SonarScannera

- **sonar-project.properties**: kluczowy plik konfiguracyjny SonarScannera
  z informacjami o projekcie, np. klucz, nazwa i URL serwera SonarQube.
- **Zmienne środowiskowe**: część właściwości można ustawić przez zmienne,
  np. `SONAR_HOST_URL`.
- **Parametry CLI**: podczas uruchamiania można przekazywać właściwości
  także bezpośrednio przez flagi.

## 4. Typowe właściwości konfiguracyjne

- `sonar.projectKey`: unikalny identyfikator projektu.
- `sonar.projectName`: nazwa projektu.
- `sonar.projectVersion`: wersja projektu.
- `sonar.sources`: katalog ze źródłami do analizy.
- `sonar.host.url`: adres serwera SonarQube (np. `http://localhost:9000`).

## 5. Uruchamianie SonarScannera

- **Maven**: `mvn sonar:sonar`
- **Gradle**: `gradle sonarqube`
- **CLI**: `sonar-scanner`

Skaner przeanalizuje projekt i wyśle wyniki do skonfigurowanego serwera SonarQube.
