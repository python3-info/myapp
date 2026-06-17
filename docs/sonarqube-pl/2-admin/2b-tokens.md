# Tokeny

W SonarQube **tokeny** służą do uwierzytelniania i autoryzacji interakcji
z platformą, szczególnie w CI oraz w narzędziach automatyzujących.
To bezpieczny sposób komunikacji z SonarQube bez ujawniania loginów i haseł.
Tokeny są powszechnie używane do analizy projektów, dostępu do API oraz
integracji z narzędziami buildowymi i systemami CI.

## 1. Czym jest token?

Token to unikalny, bezpieczny ciąg znaków, który działa jako alternatywa
dla loginu i hasła. Podczas zadań automatycznych, takich jak uruchamianie
analizy SonarQube lub wywołania API, użytkownicy i narzędzia CI/CD mogą
używać tokenów do uwierzytelniania.

## 2. Typy tokenów

- **User Tokens**: tworzone przez użytkowników i powiązane z ich kontem.
  Uprawnienia tokenu wynikają z uprawnień użytkownika.
- **CI/CD Tokens**: tworzone do integracji i używane przez systemy build
  oraz pipeline’y CI/CD. Zwykle mają dostęp ograniczony do projektu
  i służą do automatyzacji procesów.

## 3. Tworzenie i zarządzanie tokenami

Tokeny można generować w SonarQube w sekcji **My Account > Security**.
Użytkownicy tworzą tokeny przypięte do własnego konta, które potem
wykorzystuje się do uwierzytelniania wywołań API i integracji CI/CD.

Po utworzeniu tokenu SonarQube nie przechowuje jego wartości ze względów
bezpieczeństwa, więc należy go skopiować i bezpiecznie zapisać od razu.

## 4. Unieważnianie tokenów

Jeśli token zostanie skompromitowany albo nie jest już potrzebny, można go
unieważnić w sekcji **My Account > Security**. Po unieważnieniu token
przestaje działać, a systemy zależne od niego nie będą mogły się uwierzytelnić.

## 5. Zastosowania tokenów

- **Integracja CI/CD**: automatyzacja analizy projektu w pipeline’ach.
- **Dostęp do API**: bezpieczne wywołania API, np. pobieranie raportów
  analizy albo szczegółów projektów.
- **Narzędzia zewnętrzne**: np. SonarScanner, Jenkins czy GitLab CI
  mogą używać tokenów do połączenia z SonarQube.

## 6. Bezpieczeństwo tokenów

Tokeny to bezpieczny sposób logowania bez udostępniania haseł. Nadal trzeba
traktować je jak dane wrażliwe i przechowywać bezpiecznie. Nigdy nie
udostępniaj tokenów publicznie (np. w repozytorium GitHub czy logach).

---

## Ćwiczenia

### Ćwiczenie 1: Utworzenie tokenu osobistego

**Cel:**  
Naucz się tworzyć i zarządzać tokenem osobistym w SonarQube.

**Zadania:**
1. Przejdź do **My Account > Security** w SonarQube.
2. Utwórz nowy token dla swojego konta.
3. Skopiuj token i zapisz go bezpiecznie.
4. Użyj tokenu w narzędziu takim jak **SonarScanner**, aby się uwierzytelnić
   i uruchomić analizę projektu.

---

### Ćwiczenie 2: Użycie tokenu w pipeline CI/CD

**Cel:**  
Zintegruj analizę SonarQube z pipeline CI/CD przy użyciu tokenu.

**Zadania:**
1. Utwórz token w **My Account > Security**.
2. Skonfiguruj system CI/CD (np. Jenkins lub GitLab), aby używał tokenu
   do analizy SonarQube.
3. Uruchom build i sprawdź, że analiza SonarQube działa poprawnie z tokenem.

---

### Ćwiczenie 3: Unieważnienie starego tokenu

**Cel:**  
Naucz się unieważniać token, który nie jest już potrzebny.

**Zadania:**
1. Przejdź do **My Account > Security** i znajdź wcześniej utworzony token.
2. Unieważnij token.
3. Sprawdź, że token jest już nieważny, próbując użyć go do dostępu API
   albo uruchomienia analizy.
