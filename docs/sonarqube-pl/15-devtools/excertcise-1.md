# Konfiguracja importu wyników Pylint

## Cel 
 
Naucz się integrować wyniki **Pylint** z SonarQube.

## Zadania

1. Uruchom analizę **Pylint** dla projektu Python i wygeneruj raport XML.
2. W pliku `sonar-project.properties` ustaw
   `sonar.python.pylint.reportPaths`, wskazując raport Pylint XML.
3. Uruchom SonarScanner i sprawdź, czy issue z **Pylint** pojawiają się
   na dashboardzie SonarQube.
