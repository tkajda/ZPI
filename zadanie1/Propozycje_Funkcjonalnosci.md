# Propozycje Funkcjonalności Systemu LMS
*Oparte na raporcie "Najskuteczniejsze Metody Przyswajania Wiedzy"*

Dokument ten tłumaczy teoretyczne metody nauczania na konkretne funkcje systemowe, które można zaimplementować w projekcie.

## 1. Implementacja Spaced Repetition (Rozłożone powtórki)

### Funkcja: "Inteligentny Asystent Powtórek" (Smart Review Assistant)
*   **Opis:** System automatycznie generuje "talię" fiszek lub pytań na dany dzień dla każdego użytkownika, bazując na jego wcześniejszych wynikach.
*   **Mechanizm:** Algorytm (np. wariacja SuperMemo-2 lub Leitner System) oblicza optymalny czas kolejnej powtórki dla każdego elementu wiedzy.
    *   Jeśli użytkownik odpowiedział poprawnie: powtórka za 3 dni -> 7 dni -> 14 dni.
    *   Jeśli błędnie: powtórka jutro.
*   **User Story:** "Jako pracownik, chcę codziennie rano otrzymać zestaw 5-10 szybkich pytań z materiału, który przerabiałem w zeszłym tygodniu, aby utrwalić wiedzę."

## 2. Implementacja Active Recall (Aktywne przypominanie)

### Funkcja: "Interaktywne Wideo" (Video Checkpoints)
*   **Opis:** Odtwarzacz wideo zatrzymuje się w kluczowych momentach i wymusza interakcję.
*   **Mechanizm:** Zamiast pasywnego oglądania 10-minutowego filmu, system pauzuje co 2-3 minuty i zadaje pytanie otwarte lub wielokrotnego wyboru. Użytkownik nie może przejść dalej bez próby odpowiedzi.
*   **User Story:** "Jako pracownik, chcę być odpytywany w trakcie oglądania szkolenia, aby upewnić się, że rozumiem oglądany materiał."

## 3. Implementacja Learning by Doing (Nauka przez praktykę)

### Funkcja: "Wirtualne Laboratoria" (Code Sandboxes)
*   **Opis:** Zintegrowane środowisko programistyczne w przeglądarce.
*   **Mechanizm:** Użytkownik otrzymuje zadanie (np. "Napisz funkcję w Pythonie sortującą listę") i musi wpisać kod w oknie przeglądarki. System automatycznie uruchamia testy jednostkowe (Unit Tests) w tle, aby sprawdzić poprawność rozwiązania.
*   **User Story:** "Jako programista, chcę rozwiązywać zadania praktyczne bezpośrednio na platformie, bez konieczności konfigurowania środowiska lokalnego."

## 4. Implementacja Gamification (Grywalizacja)

### Funkcja: "Drzewo Umiejętności" (Skill Tree Visualization)
*   **Opis:** Wizualizacja postępów w formie grafu, inspirowana grami RPG.
*   **Mechanizm:** Użytkownik widzi "zablokowane" (szare) i "odblokowane" (kolorowe) węzły. Aby odblokować "Zaawansowany React", musi najpierw ukończyć węzły "JavaScript Basics" i "React Fundamentals".
*   **User Story:** "Jako pracownik, chcę widzieć jasną ścieżkę rozwoju i zależności między umiejętnościami, aby wiedzieć, czego uczyć się w następnej kolejności."

## 5. Implementacja Microlearning & Just-in-Time

### Funkcja: "Baza Wiedzy Problem-Solution"
*   **Opis:** Wyszukiwarka zoptymalizowana pod kątem rozwiązywania konkretnych problemów, a nie nazw kursów.
*   **Mechanizm:** Materiały wideo są automatycznie dzielone na rozdziały (chapters) i tagowane. Wyszukanie frazy "jak zresetować hasło w linux" przenosi użytkownika dokładnie do 3:45 minuty konkretnego szkolenia.
*   **User Story:** "Jako administrator, chcę szybko znaleźć fragment wideo pokazujący konkretną komendę, bez konieczności oglądania całego godzinnego szkolenia."

## 6. Implementacja Social Learning

### Funkcja: "Wyzwania Zespołowe" (Team Challenges)
*   **Opis:** Rywalizacja lub kooperacja między zespołami.
*   **Mechanizm:** Zespoły zbierają punkty za ukończone kursy i certyfikaty. Rankingi "Najlepiej wyszkolony zespół miesiąca".
*   **User Story:** "Jako Tech Lead, chcę widzieć postępy mojego zespołu na tle innych działów, aby motywować ich do rozwoju."
