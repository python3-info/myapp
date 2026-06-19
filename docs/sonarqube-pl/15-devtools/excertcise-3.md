# Import wyników bezpieczeństwa Bandit

## Cel 
 
Zaimportuj wyniki analizy bezpieczeństwa **Bandit** do SonarQube.

## Zadania

1. Uruchom **Bandit** dla projektu Python i wygeneruj raport.
2. Dodaj ścieżkę do raportu Bandit w `sonar-project.properties`
   przez właściwość `sonar.python.bandit.reportPaths`.
3. Uruchom SonarScanner i sprawdź sekcję **Security** w SonarQube,
   aby zweryfikować wykryte podatności.
