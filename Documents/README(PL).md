## Opis projektu

### Cel:

Projekt "Minesweeper Game" ma na celu stworzenie gry logicznej, która polega na odkrywaniu pól na planszy, unikając min. Gra wymaga od gracza umiejętności logicznego myślenia i planowania. Celem projektu jest dostarczenie graczom satysfakcjonującej rozgrywki, która będzie zarówno wciągająca, jak i wyzwalająca ich intelektualne umiejętności.

### Opis funkcji:

- **Rozgrywka:** Użytkownik odkrywa pola na planszy, starając się unikać min. Każde odkryte pole może zawierać wskazówki dotyczące liczby min znajdujących się w sąsiednich polach.
- **Poziomy trudności:** Gracz może wybrać poziom trudności, który wpływa na wielkość planszy oraz liczbę min.
- **Zapis gry:** Możliwość zapisywania stanu gry oraz kontynuowania jej w dowolnym momencie.
- **Tablica wyników:** Śledzenie najlepszych wyników graczy i prezentowanie ich na tablicy rekordów.
- **Tryb treningowy:** Tryb, w którym gracz może ćwiczyć bez ryzyka przegranej, idealny dla nowych graczy uczących się zasad.

## Analiza wymagań:

### Wymagania funkcjonalne:

- **Odkrywanie pól:** Użytkownik może klikać na pola planszy, aby je odkryć. Odkryte pole może być puste, zawierać liczbę wskazującą na ilość min w sąsiednich polach, lub być miną (co kończy grę).
- **Poziomy trudności:** Użytkownik może wybrać spośród kilku poziomów trudności, które różnią się wielkością planszy i liczbą min.
- **Zapis i odczyt gry:** Gra powinna umożliwiać zapisanie aktualnego stanu i wznowienie go później.
- **Tablica wyników:** Aplikacja powinna przechowywać i prezentować najlepsze czasy ukończenia gry dla różnych poziomów trudności.
- **Tryb treningowy:** Użytkownik może grać w trybie, który pozwala na naukę gry bez kończenia jej w przypadku odkrycia miny.

### Wymagania niefunkcjonalne:

- **Intuicyjność interfejsu:** Gra powinna być łatwa do nauki i obsługi, z intuicyjnym interfejsem użytkownika.
- **Wydajność:** Gra powinna działać płynnie, bez opóźnień, nawet na urządzeniach o niższej mocy obliczeniowej.
- **Estetyka:** Grafika gry powinna być przejrzysta i estetyczna, z wyraźnymi oznaczeniami pól oraz czytelnymi liczbami.
- **Dostępność:** Gra powinna być dostępna na różnych platformach (np. przeglądarki internetowe, urządzenia mobilne).

## Projekt interfejsu:

### Szkice/wizualizacje interfejsu:

- _Strona główna:_ Ekran z wyborem poziomu trudności, dostępem do tablicy wyników oraz opcją włączenia trybu treningowego.
- _Okno gry:_ Plansza gry z polami do odkrywania, licznik min pozostałych do odkrycia oraz licznik czasu.
- _Tablica wyników:_ Lista najlepszych wyników wraz z czasami dla każdego poziomu trudności.
- _Ekran końca gry:_ Powiadomienie o wygranej lub przegranej, z możliwością ponownego rozpoczęcia gry lub powrotu do strony głównej.

### Mapa strony:

- _Strona główna_
  - Wybór poziomu trudności
  - Opcja trybu treningowego
  - Dostęp do tablicy wyników
- _Okno gry_
  - Plansza gry
  - Liczniki min i czasu
  - Opcje zapisu i powrotu do menu
- _Tablica wyników_
  - Przegląd najlepszych wyników
  - Możliwość usuwania i resetowania wyników

## Architektura systemu:

### Opis struktury danych:

Aplikacja przechowuje dane związane z grą, w tym:

- **Plansza:** Macierz zawierająca informacje o minach i odkrytych polach.
- **Stan gry:** Aktualny stan rozgrywki, w tym czas gry, odkryte pola i pozostałe miny.
- **Wyniki:** Zbiór danych o najlepszych wynikach dla różnych poziomów trudności.

### Diagramy architektury:

Architektura systemu jest oparta na wzorcu Model-View-Controller (MVC), gdzie:

- **Model:** Przechowuje logikę gry, informacje o planszy, oraz wyniki.
- **Widok (View):** Odpowiada za prezentowanie interfejsu użytkownika i interakcji z graczem.
- **Kontroler (Controller):** Zarządza logiką gry, przetwarza dane z modelu i przekazuje je do widoku.

## Implementacja:

### Opis technologii:

- **Frontend:** HTML, CSS, JavaScript (React.js) - do interfejsu użytkownika i logiki gry.
- **Backend:** Flask (Python) - do obsługi zapisów gier i tablicy wyników, jeżeli będzie to aplikacja z backendem.
- **Baza danych:** SQLite lub inna lekka baza danych - do przechowywania wyników gier.

### Struktura kodu:

- _Katalogi/pliki_:
  - Oddzielne pliki dla logiki gry (np. odkrywanie pól, sprawdzanie min), interfejsu użytkownika (komponenty React), oraz zarządzania danymi (zapisywanie wyników).
- _Style pisania kodu_: Zastosowanie najlepszych praktyk, takich jak modularność, łatwość w rozszerzaniu funkcjonalności oraz dodawanie odpowiednich komentarzy w kodzie.

## Testowanie:

### Plan testów:

- **Testy jednostkowe:** Sprawdzenie poprawności funkcji związanych z logiką gry, takich jak odkrywanie pól i liczenie min.
- **Testy integracyjne:** Weryfikacja, czy wszystkie elementy gry działają prawidłowo razem, np. logika gry i interfejs użytkownika.
- **Testy interfejsu użytkownika:** Testowanie interakcji użytkownika z grą na różnych urządzeniach i przeglądarkach.
- **Testy wydajnościowe:** Ocena, jak gra radzi sobie z większymi planszami lub na starszych urządzeniach.

### Procedury testowania:

- Opracowanie przypadków testowych dla różnych scenariuszy, takich jak wykrycie miny, poprawne działanie liczników, itp.
- Testowanie na różnych platformach (PC, urządzenia mobilne) w celu zapewnienia zgodności.

## Wdrożenie i konserwacja:

### Plan wdrożenia:

- **Etapy wdrażania:**
  - Testy beta z ograniczoną grupą użytkowników
  - Poprawki na podstawie feedbacku
  - Publikacja gry na docelowych platformach (np. App Store, Google Play, strony internetowe)
- **Terminy:** Ustalenie realistycznych dat dla każdego etapu wdrożenia.

### Procedury konserwacji:

- **Wsparcie techniczne:** Zapewnienie użytkownikom kanałów do zgłaszania błędów i sugestii dotyczących gry.
- **Aktualizacje:** Regularne aktualizacje w celu dodawania nowych funkcji, poprawy wydajności oraz naprawy błędów zgłaszanych przez użytkowników.

## Harmonogram:

### Plan projektu:

- **Etapy realizacji:**
  - Projektowanie interfejsu i logiki gry
  - Implementacja funkcji podstawowych (odkrywanie pól, logika gry)
  - Testowanie gry i optymalizacja
  - Przygotowanie do wdrożenia i publikacja
- **Terminy:** Ustalenie czasu potrzebnego na każdy etap, z uwzględnieniem marginesu na poprawki.

## Kosztorys:

### Szacunkowe koszty:

- **Rozwój aplikacji:** Koszty związane z programowaniem, projektowaniem interfejsu, oraz testowaniem.
- **Koszty utrzymania:** Hosting, aktualizacje, wsparcie techniczne oraz ewentualne opłaty za usługi zewnętrzne (np. serwery, jeżeli gra wymaga backendu).

---

[English](/README.md)
