# ZPI - Zadanie 1: Drivery Architektoniczne

**Temat:** Zarządzanie cyklem życia pracownika: Strategie rekrutacji i rozwoju
**Autor:** Radosław Grędel

---

## 1. Wizja i zakres projektu

### Problem biznesowy i szanse rynkowe
W dynamicznie zmieniającym się świecie technologii, firmy IT borykają się z problemem szybkiej dezaktualizacji kompetencji swoich zespołów. Poleganie na zewnętrznych konsultantach i szkoleniach jest kosztowne i nie zawsze odpowiada specyficznym potrzebom organizacji. Istnieje potrzeba wewnętrznego systemu, który nie tylko dostarcza wiedzę, ale systematyzuje rozwój pracowników zgodnie ze strategią firmy.

### Wizja produktu
Stworzenie inteligentnej platformy LMS (Learning Management System), która przekształca organizację w środowisko ciągłego uczenia się ("Learning Organization"), gdzie każdy pracownik ma dostęp do spersonalizowanej ścieżki rozwoju (Learning Path) bezpośrednio powiązanej z celami biznesowymi firmy i wymaganiami projektowymi.

### Główny cel biznesowy (SMART)
**Zamykanie luk kompetencyjnych (Upskilling):**
Przeszkolenie 60% kadry technicznej z nowych technologii chmurowych w ciągu 12 miesięcy od wdrożenia systemu, co pozwoli na redukcję wydatków na zewnętrznych konsultantów o 200 tys. PLN rocznie, dzięki platformie LMS sugerującej spersonalizowane ścieżki rozwoju.

### Kluczowe metryki sukcesu (KPIs)
1.  **Odsetek przeszkolonej kadry:** > 60% pracowników technicznych ukończyło przypisane ścieżki "Cloud Technologies" w ciągu 12 miesięcy.
2.  **Redukcja kosztów zewnętrznych:** Zmniejszenie faktur za usługi konsultingowe o min. 200 000 PLN w skali roku po wdrożeniu.
3.  **Wskaźnik ukończenia kursów (Completion Rate):** Średni poziom ukończenia rozpoczętych kursów na poziomie > 85%.

### Główne klasy użytkowników i interesariusze

**Interesariusze:**
*   **CTO (Chief Technology Officer):** Sponsor projektu, zależy mu na kompetencjach zespołu.
*   **Dział HR:** Odpowiedzialny za rozwój pracowników i budżet szkoleniowy.

**Persony:**

**1. Anna, HR Manager (35 lat)**
*   **Cel:** Chce efektywnie zarządzać budżetem szkoleniowym i widzieć realne efekty inwestycji w rozwój pracowników.
*   **Frustracja:** Brak narzędzi do weryfikacji, czy pracownicy faktycznie korzystają z wykupionych kursów i czy przekłada się to na ich pracę.
*   **Cytat:** "Chcę mieć pewność, że pieniądze wydane na szkolenia wracają do firmy w postaci lepszych kompetencji."

**2. Piotr, Senior Developer (29 lat)**
*   **Cel:** Chce pogłębiać swoją wiedzę techniczną bez tracenia czasu na szukanie wartościowych materiałów.
*   **Frustracja:** Zbyt wiele niespójnych źródeł wiedzy, brak jasnej ścieżki awansu powiązanej z konkretnymi umiejętnościami.
*   **Cytat:** "Chcę wiedzieć, czego dokładnie muszę się nauczyć, aby awansować na architekta, i mieć do tego materiały w jednym miejscu."

---

## 2. Kluczowe wymagania i priorytetyzacja dla MVP

### Wymagania użytkownika (User Stories)

1.  **[US-1] Przeglądanie katalogu:** Jako pracownik, chcę przeglądać katalog dostępnych ścieżek rozwoju (Learning Paths), aby wybrać te zgodne z moimi zainteresowaniami.
2.  **[US-2] Przypisywanie ścieżek:** Jako Manager, chcę przypisać konkretną ścieżkę rozwoju mojemu podwładnemu, aby ukierunkować jego rozwój na potrzeby projektu.
3.  **[US-3] Odtwarzanie wideo:** Jako pracownik, chcę oglądać materiały wideo w ramach kursu, aby zdobywać nową wiedzę.
4.  **[US-4] Weryfikacja wiedzy (Quiz):** Jako pracownik, chcę rozwiązać test sprawdzający po module, aby potwierdzić zdobyte umiejętności.
5.  **[US-5] Raportowanie postępów:** Jako HR Manager, chcę generować raporty postępów zespołów, aby monitorować realizację celu 60% przeszkolonej kadry.
6.  **[US-6] Certyfikacja:** Jako pracownik, chcę otrzymać certyfikat po ukończeniu ścieżki, aby mieć dowód moich kompetencji.
7.  **[US-7] Inteligentny Asystent Powtórek:** Jako pracownik, chcę otrzymywać codzienne, krótkie zestawy pytań (Spaced Repetition), aby utrwalać wiedzę w optymalnych odstępach czasu.
8.  **[US-8] Interaktywne Wideo:** Jako pracownik, chcę odpowiadać na pytania w trakcie oglądania wideo (Active Recall), aby na bieżąco weryfikować zrozumienie materiału.
9.  **[US-9] Wirtualne Laboratoria:** Jako programista, chcę rozwiązywać zadania praktyczne w przeglądarce (Code Sandbox), aby uczyć się przez praktykę bez konfiguracji środowiska.
10. **[US-10] Drzewo Umiejętności:** Jako pracownik, chcę widzieć wizualizację moich postępów w formie drzewa (Gamification), aby wiedzieć, jakie umiejętności muszę jeszcze odblokować.

### Priorytetyzacja wymagań dla MVP

Skala: 1-21 (Fibonacci).
Priorytet = (Korzyść + Kara) / (Koszt + Ryzyko)

| ID | Funkcja | Korzyść | Kara | Koszt | Ryzyko | Priorytet | Decyzja |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| US-1 | Przeglądanie katalogu | 8 | 5 | 3 | 2 | **2.6** | **MVP** |
| US-2 | Przypisywanie ścieżek | 13 | 8 | 5 | 3 | **2.6** | **MVP** |
| US-3 | Odtwarzanie wideo | 21 | 21 | 8 | 5 | **3.2** | **MVP** |
| US-4 | Weryfikacja wiedzy (Quiz) | 13 | 8 | 5 | 2 | **3.0** | **MVP** |
| US-5 | Raportowanie postępów | 13 | 13 | 8 | 5 | **2.0** | **MVP** |
| US-6 | Certyfikacja (PDF) | 5 | 2 | 3 | 1 | **1.75** | Backlog |
| US-7 | Asystent Powtórek | 13 | 5 | 5 | 3 | **2.25** | **MVP** |
| US-8 | Interaktywne Wideo | 13 | 8 | 5 | 2 | **3.0** | **MVP** |
| US-9 | Wirtualne Laboratoria | 21 | 13 | 13 | 8 | **1.6** | Backlog |
| US-10 | Drzewo Umiejętności | 8 | 3 | 5 | 2 | **1.57** | Backlog |

**Uzasadnienie MVP:**
Do realizacji głównego celu biznesowego (przeszkolenie kadry i monitoring tego procesu) niezbędne są funkcje dostarczania treści (wideo), weryfikacji (quizy) oraz analityki (raporty).
Zdecydowano się również włączyć do MVP **Interaktywne Wideo** oraz **Asystenta Powtórek**, ponieważ badania wskazują, że są to kluczowe mechanizmy zwiększające retencję wiedzy, co bezpośrednio przekłada się na ROI projektu.
Wirtualne Laboratoria i Drzewo Umiejętności, mimo wysokiej wartości, są zbyt kosztowne i ryzykowne na etap MVP.

---

## 3. Specyfikacja atrybutów jakościowych

### Wybór atrybutów
1.  **Wydajność:** Kluczowa dla komfortu nauki (płynne wideo).
2.  **Dostępność:** Pracownicy uczą się w różnych porach, system musi być zawsze dostępny.
3.  **Modyfikowalność:** Łatwość dodawania nowych formatów szkoleń w przyszłości.

### Scenariusze jakościowe

#### 1. Wydajność (Performance)
| Element | Opis |
| :--- | :--- |
| **Źródło bodźca** | Użytkownik (Pracownik). |
| **Bodziec** | Uruchomienie materiału wideo w wysokiej rozdzielczości (1080p). |
| **Artefakt** | Moduł odtwarzacza wideo i Content Delivery Network (CDN). |
| **Środowisko** | Normalne warunki pracy, łącze biurowe lub domowe. |
| **Reakcja** | Wideo rozpoczyna odtwarzanie (buforowanie zakończone). |
| **Miara reakcji** | Czas startu wideo (Time to First Frame) **< 2 sekundy**. |

#### 2. Dostępność (Availability)
| Element | Opis |
| :--- | :--- |
| **Źródło bodźca** | Użytkownik. |
| **Bodziec** | Próba zalogowania się do platformy w celu odbycia szkolenia. |
| **Artefakt** | System uwierzytelniania i główny interfejs aplikacji. |
| **Środowisko** | Godziny poza pracą (wieczory, weekendy), kiedy pracownicy często się doszkalają. |
| **Reakcja** | System poprawnie loguje użytkownika i wyświetla dashboard. |
| **Miara reakcji** | Dostępność systemu na poziomie **99.5%** w skali miesiąca (maks. ~3.5h niedostępności). |

#### 3. Modyfikowalność (Modifiability)
| Element | Opis |
| :--- | :--- |
| **Źródło bodźca** | Deweloper / Administrator treści. |
| **Bodziec** | Konieczność dodania nowego typu zadania interaktywnego (np. "Code Challenge" - edytor kodu w przeglądarce). |
| **Artefakt** | Moduł lekcji i silnik renderowania treści. |
| **Środowisko** | Faza rozwoju (maintenance). |
| **Reakcja** | Implementacja i wdrożenie nowego typu komponentu bez zmian w jądrze systemu. |
| **Miara reakcji** | Czas implementacji i wdrożenia zmian **< 16 roboczogodzin** (2 mandays). |

### Analiza kompromisów (dla Wydajności)
*   **Cel:** Szybkie ładowanie wideo (< 2s).
*   **Rozwiązanie:** Użycie zewnętrznego, płatnego CDN (Content Delivery Network) oraz adaptacyjnego streamingu (HLS/DASH).
*   **Kompromis:**
    *   (+) Zwiększona **wydajność** i skalowalność (odciążenie głównego serwera).
    *   (-) Zwiększony **koszt** operacyjny (opłaty za transfer CDN).
    *   (-) Zależność od zewnętrznego dostawcy (ryzyko awarii trzeciej strony).

---

## 4. Ograniczenia i założenia projektowe

### 4.1. Ograniczenia

1.  **Ograniczenie budżetowe (Infrastruktura):**
    *   **Treść:** Miesięczny koszt utrzymania infrastruktury chmurowej nie może przekroczyć 2000 PLN w fazie MVP.
    *   **Wpływ:** Wymusza optymalizację przechowywania wideo (np. kompresja) i dobór efektywnych kosztowo usług (np. AWS S3 + CloudFront z limitami, lub tańsze alternatywy jak Vimeo Pro do hostingu wideo).

2.  **Ograniczenie prawne (RODO):**
    *   **Treść:** System przechowuje dane o postępach pracowników, które mogą być podstawą do oceny pracowniczej.
    *   **Wpływ:** Konieczność implementacji ścisłych ról dostępu (ACL) – Manager widzi tylko swój zespół. Logi audytowe dostępu do danych osobowych są obowiązkowe. Dane muszą być szyfrowane w spoczynku i w transmisji.

### 4.2. Założenia

1.  **Założenie:** Dostępność materiałów szkoleniowych.
    *   **Treść:** Zakładamy, że dział HR/Tech Leadzi dostarczą gotowe materiały wideo i pytania do quizów przed uruchomieniem systemu.
    *   **Ryzyko:** Jeśli materiały nie będą gotowe, platforma będzie pusta ("Ghost Town"), co zniechęci pierwszych użytkowników.
    *   **Walidacja:** Weryfikacja stanu materiałów na 2 tygodnie przed startem MVP (Milestone: Content Freeze).

2.  **Założenie:** Przepustowość sieci w biurze.
    *   **Treść:** Zakładamy, że firmowa sieć wytrzyma obciążenie, gdy wielu pracowników jednocześnie uruchomi wideo szkoleniowe (np. w "piątki rozwojowe").
    *   **Ryzyko:** Zator sieci, buforowanie wideo, frustracja użytkowników.
    *   **Walidacja:** Testy obciążeniowe sieci wewnętrznej (symulacja ruchu) przed wdrożeniem. Ewentualne wdrożenie lokalnego serwera cache'ującego w biurze.
