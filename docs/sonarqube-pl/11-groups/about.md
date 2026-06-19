# Zarządzanie grupami

Zarządzanie grupami w SonarQube pozwala administratorom organizować
użytkowników według ról, zespołów lub odpowiedzialności. Upraszcza to
kontrolę dostępu i uprawnienia, ponieważ nadaje się je na poziomie grupy,
a nie pojedynczych osób. Dzięki temu właściwe osoby mają dostęp do
właściwych projektów i funkcji.

## 1. Czym są grupy?

Grupa to zbiór użytkowników o podobnych rolach lub odpowiedzialnościach
w SonarQube. Przykładowo mogą istnieć grupy dla zespołów
(np. **Frontend Team**, **Backend Team**, **QA Team**) lub ról
(np. **Administrators**, **Developers**, **Reviewers**).

## 2. Tworzenie i zarządzanie grupami

Administratorzy mogą tworzyć własne grupy, by efektywniej zarządzać
dostępem i uprawnieniami. Każda grupa może mieć inne role, a członkowie
dziedziczą przypisane role i uprawnienia.

- Aby utworzyć grupę, przejdź do **Administration > Security > Groups** i kliknij **Create Group**.
- Po utworzeniu grupy użytkowników można dodać ręcznie albo zbiorczo.

## 3. Przypisywanie ról do grup

Grupom można przypisywać role określające, jakie działania ich członkowie
mogą wykonywać w SonarQube. Występują dwa główne typy ról:

- **Global Roles**: dotyczą całej instancji SonarQube
  (np. **Administrator**, **User**).
- **Project Roles**: dotyczą konkretnego projektu
  (np. **Developer**, **Viewer**, **Project Lead**).

Przypisywanie ról do grup upraszcza zarządzanie uprawnieniami. Na przykład
rola **Developer** dla grupy **Frontend Team** daje dostęp do funkcji
deweloperskich bez dostępu administracyjnego.

## 4. Uprawnienia i kontrola dostępu

- **Global Permissions**: np. **Administer System**, **View System** itp.
- **Project Permissions**: np. **Administer Project**,
  **Browse Project**, **Analyze Code** itd.

Łącząc użytkowników z grupami i przypisując odpowiednie role,
administratorzy zapewniają poprawny poziom dostępu.

## 5. Audyt i monitoring

SonarQube oferuje również audit logs do śledzenia zmian związanych z grupami.
Administratorzy mogą monitorować dodawanie i usuwanie użytkowników z grup
oraz zmiany ról i uprawnień grup.
