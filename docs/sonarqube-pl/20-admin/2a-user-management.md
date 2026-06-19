# Zarządzanie użytkownikami

Zarządzanie użytkownikami w SonarQube pozwala administratorom zarządzać i
konfigurować poziomy dostępu użytkowników, grup i ról w platformie.
Skuteczne zarządzanie użytkownikami zapewnia, że właściwe osoby mają
odpowiedni dostęp do projektów, issue i konfiguracji, co pomaga
utrzymywać bezpieczeństwo i kontrolę nad procesem wytwarzania.

## 1. Użytkownicy

Użytkownicy w SonarQube reprezentują konkretne osoby mające dostęp do
systemu. Konta mogą być tworzone ręcznie lub przez integrację z
zewnętrznymi systemami uwierzytelniania (np. LDAP, SSO).

- **Admin Users**: zwykle mają pełny dostęp do funkcji i administracji.
- **Regular Users**: mogą analizować projekty, przeglądać issue i
  uczestniczyć w analizie jakości, ale często mają ograniczony dostęp
  do ustawień systemowych.
- **Guest Users**: zwykle mają dostęp tylko do odczytu.

## 2. Grupy

Grupy w SonarQube służą do organizowania użytkowników, najczęściej według
ról w procesie developmentu. Dzięki grupom administratorzy mogą łatwo
zarządzać uprawnieniami wielu użytkowników naraz.

- **Default Groups**: SonarQube udostępnia grupy domyślne, takie jak
  `sonar-users` (dla zwykłych użytkowników) i `sonar-administrators`
  (dla administratorów).
- **Custom Groups**: można tworzyć grupy własne dla konkretnych zespołów
  (np. frontend, backend, security) i poziomów dostępu.

## 3. Role i uprawnienia

Role definiują, jakie działania użytkownicy i grupy mogą wykonywać w
SonarQube. Uprawnienia mogą być nadawane globalnie albo na poziomie projektu.

- **Global Permissions**: obejmują uprawnienia administracyjne, takie jak
  zarządzanie konfiguracją globalną, użytkownikami i ustawieniami systemu.
- **Project Permissions**: obejmują uprawnienia dla konkretnego projektu,
  np. podgląd dashboardu, zarządzanie konfiguracją projektu i uruchamianie analiz.

## 4. Uwierzytelnianie i autoryzacja

SonarQube wspiera zarówno **internal authentication** (konta przechowywane
w SonarQube), jak i **external authentication** (integracje z LDAP,
Active Directory lub SSO). Zewnętrzne uwierzytelnianie ułatwia centralne
zarządzanie użytkownikami, szczególnie w większych organizacjach.

## 5. Interfejs zarządzania użytkownikami i grupami

Administratorzy mogą zarządzać użytkownikami i grupami w menu
**Administration > Security > Users** oraz
**Administration > Security > Groups**. Z tego poziomu można tworzyć,
edytować i usuwać użytkowników, przypisywać ich do grup oraz nadawać role.

## 6. Audit Logs

SonarQube udostępnia także audit logs, które śledzą działania użytkowników,
np. próby logowania, zmiany konfiguracji i modyfikacje uprawnień.
To wspiera bezpieczeństwo i rozliczalność działań.

## Ćwiczenia

## Ćwiczenie 1: Przeglądanie i zarządzanie profilami użytkowników

## Cel 
 
Naucz się przeglądać i zarządzać profilami użytkowników w SonarQube.

## Zadania

1. Przejdź do sekcji **User Management** w interfejsie SonarQube.
2. Wyszukaj użytkownika po nazwie lub loginie.
3. Wybierz użytkownika i sprawdź informacje profilu, takie jak:
   - Username
   - Email
   - Last connection
   - Assigned projects (jeśli dotyczy)
4. Zaktualizuj **email address** i **password** użytkownika.
5. Zapisz zmiany.

## Ćwiczenie 2: Tworzenie i usuwanie użytkowników

## Cel 
 
Naucz się tworzyć i dezaktywować konta użytkowników w SonarQube.

## Zadania

1. Przejdź do sekcji **User Management** w interfejsie SonarQube.
2. Utwórz nowego użytkownika „bob” z hasłem „Abcdefghi!23” i nazwą „Bob”.
3. Dezaktywuj konto „bob”, usuwając użytkownika.

## Ćwiczenie 3: Wyszukiwanie użytkowników i filtrowanie wyników

## Cel 
 
Naucz się efektywnie wyszukiwać i filtrować listę użytkowników.

## Zadania

1. Przejdź do sekcji **User Management**.
2. Użyj paska wyszukiwania, aby znaleźć użytkowników według kryteriów:
   - Username
   - Email
   - Last login time
3. Zastosuj dostępne filtry, aby zawęzić listę
   (np. użytkownicy, którzy nie logowali się od ponad 30 dni).
4. Sprawdź, czy wyniki wyszukiwania i filtrowania pokazują właściwe osoby.
5. Przetestuj różne kombinacje wyszukiwania i filtrów, aby doprecyzować listę.
