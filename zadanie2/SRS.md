# Specyfikacja Wymagań Oprogramowania (SRS)

**Tytuł Projektu:** Intelligent LMS
**Wersja:** 0.1.0
**Zespół:** Zespół Projektowy ZPI

---

## 1. Wstęp

### 1.1. Cel
Celem niniejszego dokumentu jest zdefiniowanie wymagań funkcjonalnych i niefunkcjonalnych dla systemu "Intelligent LMS". Dokument ten służy jako podstawa do prac projektowych, implementacyjnych oraz testowych. Jest przeznaczony dla zespołu deweloperskiego, kierowników projektu oraz interesariuszy biznesowych (CTO, HR).

### 1.2. Wizja, Zakres i Cele Produktu
**Wizja:**
Stworzenie inteligentnej platformy LMS (Learning Management System), która przekształca organizację w środowisko ciągłego uczenia się ("Learning Organization"), gdzie każdy pracownik ma dostęp do spersonalizowanej ścieżki rozwoju (Learning Path) bezpośrednio powiązanej z celami biznesowymi firmy.

**Zakres:**
System będzie umożliwiał zarządzanie ścieżkami rozwoju, przydzielanie kursów, weryfikację wiedzy poprzez quizy oraz raportowanie postępów.

**Kryteria Akceptacji (KPIs):**
*   **Upskilling:** Przeszkolenie 60% kadry technicznej z nowych technologii w ciągu 12 miesięcy.
*   **Oszczędność:** Redukcja wydatków na zewnętrznych konsultantów o 200 tys. PLN rocznie.
*   **Zaangażowanie:** Wskaźnik ukończenia kursów na poziomie > 85%.

**Poza Zakresem:**
System nie będzie obsługiwał płatności za kursy (wszystkie materiały są wewnętrzne lub opłacone ryczałtem) ani rekrutacji nowych pracowników.

### 1.3. Definicje, Akronimy i Skróty
*   **LMS (Learning Management System):** System zarządzania nauczaniem.
*   **Learning Path:** Zorganizowana sekwencja kursów i materiałów mająca na celu rozwój konkretnych kompetencji.
*   **Active Recall:** Metoda nauki polegająca na aktywnym przywoływaniu informacji (np. odpowiadanie na pytania w trakcie wideo).
*   **Spaced Repetition:** Metoda nauki oparta na powtórkach rozłożonych w czasie.
*   **KPI (Key Performance Indicator):** Kluczowy wskaźnik efektywności.

### 1.4. Przegląd Dokumentu
Dokument składa się z 7 rozdziałów. Po wstępie (Rozdział 1), Rozdział 2 przedstawia ogólny opis systemu, w tym charakterystykę użytkowników. Rozdział 3 definiuje wymagania interfejsów. Kluczowy Rozdział 4 szczegółowo opisuje wymagania funkcjonalne w formacie User Stories. Rozdział 5 to wymagania niefunkcjonalne. Rozdział 6 zawiera analizę porównawczą, a Rozdział 7 dodatki, w tym diagramy.

---

## 2. Opis Ogólny

### 2.1. Główne Funkcje Produktu
System Intelligent LMS składa się z następujących głównych modułów funkcjonalnych:

*   **Zarządzanie Ścieżkami Rozwoju (Learning Paths):** Tworzenie i edycja ścieżek edukacyjnych.
*   **Katalog Kursów:** Przeglądanie i wyszukiwanie dostępnych szkoleń.
*   **Moduł Odtwarzania (Player):** Odtwarzanie wideo, w tym wideo interaktywnego (Active Recall).
*   **Weryfikacja Wiedzy:** Moduł quizów i testów sprawdzających.
*   **Inteligentny Asystent Powtórek:** System Spaced Repetition sugerujący powtórki.
*   **Raportowanie i Analityka:** Generowanie raportów dla managerów i HR.

### 2.2. Klasy Użytkowników

**Rola:** HR Manager / Administrator
*   **Opis:** Zarządza budżetem, użytkownikami i ścieżkami szkoleniowymi. Monitoruje postępy.
*   **Persona:** **Anna (35 lat)**. Cel: Chce efektywnie zarządzać budżetem szkoleniowym. Frustracja: Brak weryfikacji efektów szkoleń.

**Rola:** Pracownik / Developer
*   **Opis:** Korzysta z systemu do nauki, realizuje przypisane ścieżki.
*   **Persona:** **Piotr (29 lat)**. Senior Developer. Cel: Chce pogłębiać wiedzę techniczną bez tracenia czasu na szukanie materiałów. Frustracja: Niespójne źródła wiedzy.

**Rola:** Manager Zespołu
*   **Opis:** Przypisuje ścieżki podwładnym i monitoruje ich rozwój w kontekście potrzeb projektowych.

### 2.3. Ograniczenia Projektowe i Implementacyjne
**Technologiczne:**
*   **Budżet Infrastruktury:** Miesięczny koszt chmury max 2000 PLN (MVP). Wymusza optymalizację przechowywania wideo.

**Organizacyjne:**
*   **Zespół:** Dostępność materiałów szkoleniowych zależy od działu HR i Tech Leadów.

**Prawne i Środowiskowe:**
*   **RODO (GDPR):** System przetwarza dane osobowe i wyniki pracowników. Wymagane ścisłe role dostępu (ACL), szyfrowanie i logi audytowe.

### 2.4. Założenia Projektowe
*   **Dostępność Materiałów:** Dział HR dostarczy gotowe wideo i quizy przed startem systemu.
*   **Przepustowość Sieci:** Sieć biurowa wytrzyma obciążenie przy jednoczesnym streamingu wideo przez wielu pracowników.
*   **Skills Matrix:** Istnieje zdefiniowana macierz kompetencji, do której można mapować ścieżki.

---

## 3. Wymagania Dotyczące Interfejsów Zewnętrznych

### 3.1. Interfejsy Użytkownika (UI)
Aplikacja będzie posiadać interfejs webowy (SPA) zaprojektowany zgodnie z zasadami **Material Design**. Priorytetem jest czytelność i intuicyjność (User-Friendly).
System musi być responsywny (RWD) i obsługiwać urządzenia mobilne oraz desktopowe.

**Główne widoki:**
*   Dashboard użytkownika (Moje Ścieżki).
*   Katalog Kursów (Wyszukiwarka).
*   Odtwarzacz Wideo z panelem bocznym.

*Makiety (Low-Fi) znajdują się w katalogu `images/`.*

### 3.2. Interfejsy Programowe (API)
System będzie komunikował się z zewnętrznymi systemami:

1.  **System HR (ERP):**
    *   **Cel:** Pobieranie i aktualizacja listy pracowników, struktury organizacyjnej i stanowisk.
    *   **Protokół:** REST API / JSON.
    *   **Częstotliwość:** Synchronizacja nocna (Batch).

2.  **System Uwierzytelniania (SSO):**
    *   **Cel:** Logowanie pracowników firmowym kontem.
    *   **Protokół:** OAuth 2.0 / OpenID Connect (Azure AD).

---

## 4. Wymagania Funkcjonalne

### 4.1. Przeglądanie Katalogu (US-1)

**Opis:** Umożliwia pracownikom przeglądanie dostępnych ścieżek rozwoju i filtrowanie ich po kategoriach.
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę przeglądać katalog dostępnych ścieżek rozwoju,
*   abym mógł wybrać te zgodne z moimi zainteresowaniami.

**Cel Biznesowy:** Zwiększenie zaangażowania pracowników w samorozwój.
**Warunki Wstępne:** Użytkownik zalogowany do systemu.
**Warunki Końcowe:** Użytkownik widzi listę ścieżek.

**Kryteria Akceptacji:**

**Scenariusz Główny: Wyświetlenie katalogu**
*   **Given:** Jestem zalogowanym pracownikiem.
*   **When:** Wchodzę w zakładkę "Katalog".
*   **Then:** Widzę listę kafelków z nazwami ścieżek, poziomem trudności i czasem trwania.

### 4.2. Przypisywanie Ścieżek (US-2)

**Opis:** Manager może przypisać ścieżkę obligatoryjną swojemu podwładnemu.
**Historyjka Użytkownika:**
*   Jako Manager,
*   chcę przypisać konkretną ścieżkę rozwoju mojemu podwładnemu,
*   aby ukierunkować jego rozwój na potrzeby projektu.

**Cel Biznesowy:** Zamykanie luk kompetencyjnych w zespole.
**Warunki Wstępne:** Manager jest zalogowany i ma podpiętych członków zespołu.
**Warunki Końcowe:** Ścieżka pojawia się w "Moich Ścieżkach" pracownika z oznaczeniem "Wymagana".

**Kryteria Akceptacji:**

**Scenariusz Główny: Przypisanie ścieżki**
*   **Given:** Jestem Managerem na profilu pracownika.
*   **When:** Kliknę "Przypisz Ścieżkę" i wybiorę z listy "Java Advanced".
*   **Then:** Pracownik otrzymuje powiadomienie e-mail.
*   **And:** Ścieżka jest widoczna na koncie pracownika.

### 4.3. Odtwarzanie i Interakcja z Wideo (US-3, US-8)

**Opis:** Odtwarzacz wideo z obsługą Active Recall (pytania w trakcie oglądania).
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę odpowiadać na pytania w trakcie oglądania wideo,
*   aby na bieżąco weryfikować zrozumienie materiału.

**Cel Biznesowy:** Zwiększenie retencji wiedzy poprzez interakcję.
**Warunki Wstępne:** Użytkownik uruchomił materiał wideo.
**Warunki Końcowe:** postęp wideo zostaje zapisany.

**Kryteria Akceptacji:**

**Scenariusz Główny: Active Recall**
*   **Given:** Oglądam wideo szkoleniowe.
*   **When:** Wideo dociera do znacznika czasu z przypisanym pytaniem.
*   **Then:** Odtwarzanie jest pauzowane automatycznie.
*   **And:** Na ekranie pojawia się pytanie wielokrotnego wyboru.
*   **And:** Nie mogę wznowić odtwarzania bez udzielenia odpowiedzi.

### 4.4. Weryfikacja Wiedzy - Quiz (US-4)

**Opis:** Test sprawdzający wiedzę po zakończeniu modułu szkoleniowego.
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę rozwiązać test sprawdzający po module,
*   aby potwierdzić zdobyte umiejętności i zaliczyć kurs.

**Cel Biznesowy:** Potwierdzenie nabycia kompetencji.
**Warunki Wstępne:** Użytkownik ukończył wszystkie materiały wideo w module.
**Warunki Końcowe:** Wynik testu jest zapisany w profilu użytkownika.

**Kryteria Akceptacji:**

**Scenariusz Główny: Zaliczenie testu**
*   **Given:** Ukończyłem oglądanie materiałów w module.
*   **When:** Przystępuję do quizu i uzyskuję wynik > 80%.
*   **Then:** Moduł otrzymuje status "Zaliczony".
*   **And:** System gratuluje sukcesu i odblokowuje kolejny moduł (jeśli istnieje).

### 4.5. Raportowanie Postępów (US-5)

**Opis:** Generowanie raportów o postępach pracowników i zespołów dla działu HR.
**Historyjka Użytkownika:**
*   Jako HR Manager,
*   chcę generować raporty postępów zespołów,
*   aby monitorować realizację celu 60% przeszkolonej kadry.

**Cel Biznesowy:** Monitoring KPI projektu.
**Warunki Wstępne:** W systemie są zarejestrowane postępy użytkowników.
**Warunki Końcowe:** Manager otrzymuje plik CSV/PDF z raportem.

**Kryteria Akceptacji:**

**Scenariusz Główny: Generowanie raportu**
*   **Given:** Jestem zalogowany jako HR Manager.
*   **When:** Wybieram zakres dat i zespół, a następnie klikam "Generuj Raport".
*   **Then:** System pobiera dane o ukończonych kursach.
*   **And:** Pobieram wygenerowany plik z raportem.

### 4.6. Inteligentny Asystent Powtórek (US-7)

**Opis:** Algorytm sugerujący powtórki materiału w optymalnych odstępach czasu (SR).
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę otrzymywać codzienne, krótkie zestawy pytań,
*   aby utrwalać wiedzę w optymalnych odstępach czasu.

**Cel Biznesowy:** Zapobieganie zapominaniu (Krzywa Zapominania).
**Warunki Wstępne:** Użytkownik ukończył przynajmniej jeden moduł.
**Warunki Końcowe:** Wyniki powtórek aktualizują harmonogram kolejnych pytań.

**Kryteria Akceptacji:**

**Scenariusz Główny: Codzienna sesja powtórkowa**
*   **Given:** Mam zaplanowane powtórki na dzisiaj.
*   **When:** Loguję się do systemu i widzę powiadomienie "Czas na powtórkę".
*   **Then:** System prezentuje mi 5 szybkich pytań z materiału przerobionego w przeszłości.
*   **And:** Jeśli odpowiem błędnie, pytanie wróci do mnie szybciej (np. jutro).

### 4.1. Priorytetyzacja Wymagań
[Tabela priorytetyzacji]

---

## 5. Atrybuty Jakościowe

### Jakość Wykonania
**Wydajność:**
*   [Wymaganie]

**Dostępność:**
*   [Wymaganie]

**Bezpieczeństwo:**
*   [Wymaganie]

**Skalowalność:**
*   [Wymaganie]

### Jakość Projektu
**Modyfikowalność:**
*   [Wymaganie]

**Przenośność:**
*   [Wymaganie]

### 5.1. Priorytetyzacja Atrybutów Jakościowych
[Opis priorytetów]

---

## 6. Odkrywanie i Analiza Wymagań

### 6.1. Analiza Porównawcza
**Konkurencja:**
*   [Konkurent 1]

**Kryteria Oceny:**
[Tabela]

**Wnioski:**
[Synteza wyników]

---

## 7. Dodatki

### Dodatek A: Modele Analityczne
[Diagram Przypadków Użycia]

### Dodatek B: Persony Użytkowników
[Opis person]

### Dodatek C: Kwestie do Rozwiązania
[Pytania i niejasności]
