# Quality Gates

**Quality Gate** w SonarQube to zestaw warunków, które projekt musi
spełnić, aby został uznany za "zdrowy". Warunki te służą do pilnowania,
aby kod spełniał zdefiniowane standardy jakości. Quality Gates można
dostosowywać, np. wymagając braku krytycznych błędów i podatności
albo minimalnego poziomu pokrycia testami.  
Celem Quality Gate jest blokowanie problematycznego kodu przed
scaleniem do produkcji lub wdrożeniem.

## 1. Warunki

- **Brak issue krytycznych lub blocker**: projekt nie może mieć krytycznych
  ani blocker bugs/vulnerabilities.
- **Test coverage**: projekt musi mieć minimalny poziom pokrycia testami
  jednostkowymi (np. 80%).
- **Duplications**: poziom duplikacji kodu musi być poniżej określonego
  progu.

## 2. Status Quality Gate

- **Passed**: projekt spełnia wszystkie warunki Quality Gate.
- **Failed**: co najmniej jeden warunek nie został spełniony.
- **Unknown**: projekt nie był ostatnio analizowany lub nie spełnia jeszcze
  warunków potrzebnych do oceny.

## 3. Domyślny Quality Gate

- Brak issue blocker i critical.
- Minimalne pokrycie testami.
- Brak nowych code smells.

## 4. Niestandardowe Quality Gates

Projekty mogą mieć własne quality gates dopasowane do potrzeb. Na przykład
projekt może wymagać wyższego pokrycia testami albo ostrzejszego limitu
długu technicznego. Niestandardowe quality gates mogą być tworzone przez
administratorów i przypisywane do konkretnych projektów lub gałęzi.

## 5. Quality Gate dla Pull Requestów

SonarQube może stosować quality gates bezpośrednio do pull requestów.
Dzięki temu do gałęzi głównej trafia tylko kod spełniający standardy
jakości. Pozwala to utrzymywać wysoką jakość jeszcze przed merge.

## Zarządzanie Quality Gates

Quality gates można konfigurować i modyfikować w menu **Quality Gates**
w sekcji **Administration**. Użytkownicy mogą definiować nowe bramki,
przypisywać je do projektów i dostosowywać warunki.

---

## Ćwiczenia

### Ćwiczenie 1: Sprawdzenie statusu Quality Gate

**Cel:**  
Sprawdź status Quality Gate w projekcie.

**Zadania:**
1. Przejdź do strony **Project Overview**.
2. Znajdź wskaźnik **Quality Gate Status**.
3. Sprawdź, czy projekt zaliczył quality gate, i zanotuj przyczynę
   niezaliczenia (jeśli dotyczy).

---

### Ćwiczenie 2: Modyfikacja warunku Quality Gate

**Cel:**  
Naucz się modyfikować warunki Quality Gate.

**Zadania:**
1. Przejdź do sekcji **Quality Gates** w menu **Administration**.
2. Edytuj domyślną quality gate i zmień warunek
   (np. zwiększ wymagane pokrycie testami do 85%).
3. Zastosuj nową quality gate do wybranego projektu.

---

### Ćwiczenie 3: Konfiguracja Quality Gate dla Pull Requesta (Developer Edition)

**Cel:**  
Skonfiguruj Quality Gate dla pull requestów, aby zapewnić jakość kodu przed merge.

**Zadania:**
1. Przejdź do sekcji **Pull Requests** w projekcie.
2. Sprawdź, czy quality gate jest stosowany do przychodzących pull requestów.
3. Utwórz regułę, która odrzuca pull request, jeśli wprowadza nowe
   code smells lub obniża test coverage.
