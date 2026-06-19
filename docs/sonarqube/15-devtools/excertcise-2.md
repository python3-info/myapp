# Import wyników Coverage do SonarQube

## Cel 
 
Zintegruj wyniki **code coverage** z SonarQube.

## Zadania

1. Wygeneruj raport pokrycia za pomocą **coverage.py** lub innego narzędzia.
2. W pliku `sonar-project.properties` ustaw
   `sonar.python.coverage.reportPaths` na lokalizację raportu.
3. Uruchom SonarScanner i sprawdź zakładkę **Coverage** w SonarQube,
   aby potwierdzić, że metryki są widoczne.
