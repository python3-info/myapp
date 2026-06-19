# Uprawnienia globalne i projektowe

W SonarQube **uprawnienia** określają, jakie działania użytkownicy i grupy
mogą wykonywać w platformie. Dzielą się na **uprawnienia globalne** i
**uprawnienia projektowe**, które kontrolują dostęp na różnych poziomach.
Dzięki poprawnemu zarządzaniu uprawnieniami administratorzy mogą zapewnić
użytkownikom właściwy dostęp do konfiguracji, analiz i pracy z projektami.

## Uprawnienia globalne

Uprawnienia globalne dotyczą całej instancji SonarQube i nie są powiązane
z pojedynczym projektem. Kontrolują dostęp do funkcji systemowych i
administracyjnych.

Przykładowe uprawnienia globalne:
- **Administer System**: pełna administracja instancją SonarQube, w tym
  konfiguracja i ustawienia globalne.
- **Administer Security**: zarządzanie rolami użytkowników, grupami i
  ustawieniami bezpieczeństwa w całym systemie.
- **Create Projects**: możliwość tworzenia nowych projektów.
- **Browse**: dostęp tylko do odczytu informacji o projektach, dashboardach
  i issue bez możliwości modyfikacji.

Te uprawnienia zwykle nadaje się **administratorom** lub **superuserom**.

## Uprawnienia projektowe

Uprawnienia projektowe są bardziej szczegółowe i dotyczą wyłącznie
konkretnego projektu. Określają, co użytkownicy i grupy mogą robić
w obrębie projektu, np. uruchamiać analizę, przeglądać issue albo
zmieniać ustawienia projektu.

Przykładowe uprawnienia projektowe:
- **Administer Project**: pełna administracja projektem, w tym konfiguracja,
  reguły i zarządzanie członkami.
- **Browse Project**: dostęp tylko do odczytu dashboardu projektu, issue
  i innych szczegółów.
- **Execute Analysis**: możliwość uruchamiania analizy projektu
  (np. przez SonarScanner lub integrację CI).
- **Issue View**: możliwość przeglądania issue bez ich modyfikacji.

Uprawnienia projektowe pomagają precyzyjnie rozdzielać odpowiedzialności
w zespole.

## Zarządzanie uprawnieniami

Uprawnienia można przypisywać bezpośrednio użytkownikom lub przez grupy.
Przypisywanie grup upraszcza zarządzanie większą liczbą osób.

Uprawnieniami zarządza się w **Administration > Security > Permissions**,
gdzie administratorzy przypisują role i uprawnienia użytkownikom oraz grupom.
