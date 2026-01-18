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
Stworzenie inteligentnej platformy rozwojowo-benefitowej LMS (Learning Management System), która przekształca organizację w środowisko ciągłego uczenia się ("Learning Organization"), gdzie każdy pracownik ma dostęp do spersonalizowanej ścieżki rozwoju (Learning Path) bezpośrednio powiązanej z celami biznesowymi firmy oraz elastycznym systemem nagród.
Każda ścieżka rozwoju będzie bezpośrednio powiązana z celami firmy poprzez mechanizm OKR (Objectives and Key Results). System umożliwi kaskadowanie celów od poziomu strategicznego do celów indywidualnych, wizualizację drzewa celów oraz kwartalną weryfikację realizacji strategii.

**Zakres:**
System będzie umożliwiał zarządzanie ścieżkami rozwoju, przydzielanie kursów, weryfikację wiedzy poprzez quizy, raportowanie postępów oraz obsługę wirtualnego portfela punktowego. Kluczowym elementem jest platforma kafeteryjna, zintegrowana z dostawcami usług zewnętrznych, umożliwiająca wymianę punktów na benefity rozwojowe i prozdrowotne.

System będzie również wspierał definiowanie, kaskadowanie i monitorowanie celów OKR, wymuszając hierarchiczną strukturę danych, zapewniając mechanizmy wizualizacji drzewa celów oraz analitykę postępów powiązaną z celami biznesowymi.

**Kryteria Akceptacji (KPIs):**
*   **Upskilling:** Przeszkolenie 60% kadry technicznej z nowych technologii w ciągu 12 miesięcy.
*   **Oszczędność:** Redukcja wydatków na zewnętrznych konsultantów o 200 tys. PLN rocznie.
*   **Zaangażowanie:** Wskaźnik ukończenia kursów na poziomie > 85%.
*   **Optymalizacja Budżetu:** zwiększenie utylizacji budżetu szkoleniowo-benefitowego do 95% (z obecnych 60%) w ciągu 12 miesięcy poprzez wdrożenie platformy kafeteryjnej.

**Cele Biznesowe (OKR):**
*   **Zarządzanie przez cele (OKR):** Zapewnienie 100% transparentności powiązań między celami indywidualnymi a strategią firmy w ciągu 3 miesięcy, poprzez system kaskadowania celów OKR, co pozwoli na kwartalną weryfikację realizacji strategii. (Wymusza hierarchiczną strukturę danych, wizualizację drzewa celów i analitykę postępów.)

**Poza Zakresem:**
System nie będzie obsługiwał płatności za kursy (wszystkie materiały są wewnętrzne lub opłacone ryczałtem) ani rekrutacji nowych pracowników.

### 1.3. Definicje, Akronimy i Skróty
*   **LMS (Learning Management System):** System zarządzania nauczaniem.
*   **Learning Path:** Zorganizowana sekwencja kursów i materiałów mająca na celu rozwój konkretnych kompetencji.
*   **Active Recall:** Metoda nauki polegająca na aktywnym przywoływaniu informacji (np. odpowiadanie na pytania w trakcie wideo).
*   **Spaced Repetition:** Metoda nauki oparta na powtórkach rozłożonych w czasie.
*   **KPI (Key Performance Indicator):** Kluczowy wskaźnik efektywności.
*   **System Kafeteryjny:** Model benefitów pozwalający pracownikowi na samodzielny wybór świadczeń z udostępnionej puli usług.
*   **Portfel Wirtualny:** Moduł zarządzający saldem punktów pracownika, zdobytych za aktywność edukacyjną.

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
*   **Wirtualny Portfel i Silnik Kafeteryjny:** Moduł transakcyjny zarządzający punktami. Odpowiada za przeliczanie postępów w nauce na jednostki płatnicze i ich wymianę wewnątrz Marketplace.
*   **Zaawansowana Analityka Budżetowa:** Monitorowanie wskaźników utylizacji budżetu (KPI: 95%) oraz efektywności kosztowej programów rozwojowych.
*   **Moduł Integracji Zewnętrznych:** Automatyczna komunikacja z dostawcami usług (np. generowanie voucherów w systemach partnerów).


### 2.2. Klasy Użytkowników

**Rola:** HR Manager / Administrator
*   **Opis:** Zarządza budżetem, użytkownikami, ścieżkami szkoleniowymi i ofertą świadczonych usług. Monitoruje postępy.
*   **Persona:** **Anna (35 lat)**. Cel: Chce efektywnie zarządzać budżetem szkoleniowym. Chce widzieć pełny obraz zwrotu z inwestycji (ROI) oraz zautomatyzować proces wydawania benefitów, by uniknąć pracy w arkuszach kalkulacyjnych. Frustracja: Brak weryfikacji efektów szkoleń. Traci 5 godzin tygodniowo na przepisywanie punktów z systemu szkoleń do arkusza zamówień benefitów.

**Rola:** Pracownik / Developer
*   **Opis:** Korzysta z systemu do nauki, realizuje przypisane ścieżki.
*   **Persona:** **Piotr (29 lat)**. Senior Developer. Cel: Chce pogłębiać wiedzę techniczną bez tracenia czasu na szukanie materiałów. Chce rozwijać kompetencje techniczne i mieć realny wpływ na wybór swoich benefitów (wellness/rozwój) w ramach zdobytych punktów. Frustracja: Niespójne źródła wiedzy. Dostał kolejną kartę sportową, z której nie korzysta, a wolałby dofinansowanie do ergonomicznego fotela lub sesję z trenerem kręgosłupa.

**Rola:** Manager Zespołu
*   **Opis:** Przypisuje ścieżki podwładnym i monitoruje ich rozwój w kontekście potrzeb projektowych. Monitoruje rozwój i wellbeing podwładnych.

### 2.3. Ograniczenia Projektowe i Implementacyjne
**Technologiczne:**
*   **Budżet Infrastruktury:** Miesięczny koszt chmury max 2000 PLN (MVP). Wymusza optymalizację przechowywania wideo.
*   **Integracje API:** Konieczność obsługi zewnętrznych interfejsów dostawców usług benefitowych (np. bramki voucherowe).

**Organizacyjne:**
*   **Zespół:** Dostępność materiałów szkoleniowych zależy od działu HR i Tech Leadów.
*   **Dostawcy:** Dostępność usług w Marketplace zależy od podpisanych umów z partnerami zewnętrznymi (np. Medicover, Benefit Systems).

**Prawne i Środowiskowe:**
*   **RODO (GDPR):** System przetwarza dane osobowe i wyniki pracowników. Wymagane ścisłe role dostępu (ACL), szyfrowanie i logi audytowe.

### 2.4. Założenia Projektowe
*   **Dostępność Materiałów:** Dział HR dostarczy gotowe wideo i quizy przed startem systemu.
*   **Przepustowość Sieci:** Sieć biurowa wytrzyma obciążenie przy jednoczesnym streamingu wideo przez wielu pracowników.
*   **Skills Matrix:** Istnieje zdefiniowana macierz kompetencji, do której można mapować ścieżki.
*   **Dostępność API:** Zakłada się, że kluczowi dostawcy benefitów udostępniają stabilne środowiska API do integracji.
*   **Hybrydowa Realizacja:** Realizacja usług cyfrowych (kody, vouchery) odbywa się w czasie rzeczywistym, natomiast usługi fizyczne mogą wymagać uproszczonego potwierdzenia przez dział administracji (docelowo dążenie do 100% automatyzacji w celu osiągnięcia KPI 95% utylizacji).

---

## 3. Wymagania Dotyczące Interfejsów Zewnętrznych

### 3.1. Interfejsy Użytkownika (UI)
Aplikacja będzie posiadać interfejs webowy (SPA) zaprojektowany zgodnie z zasadami **Material Design**. Priorytetem jest czytelność i intuicyjność (User-Friendly).
System musi być responsywny (RWD) i obsługiwać urządzenia mobilne oraz desktopowe.

**Główne widoki:**

1.  **Dashboard użytkownika (Moje Ścieżki):**
    ![Dashboard](images/dashboard_mockup.png)

2.  **Katalog Kursów (Wyszukiwarka):**
    ![Katalog](images/catalog_mockup.png)

3.  **Odtwarzacz Wideo z panelem bocznym:**
    ![Odtwarzacz](images/videoplayer_mockup.png)

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

**Scenariusz Alternatywny: Brak wyników wyszukiwania**
*   **Given:** Jestem w katalogu kursów.
*   **When:** Wpisuję w wyszukiwarkę frazę "Programowanie w COBOL", której nie ma w bazie.
*   **Then:** Lista kursów jest pusta.
*   **And:** Wyświetla się komunikat "Nie znaleziono kursów dla podanej frazy".
*   **And:** System sugeruje "Wyczyść filtry" lub "Zgłoś zapotrzebowanie na kurs".

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

**Scenariusz Wyjątkowy: Próba przypisania już posiadanej ścieżki**
*   **Given:** Jestem na profilu pracownika, który ma już przypisaną ścieżkę "Java Advanced".
*   **When:** Próbuję ponownie przypisać tę samą ścieżkę.
*   **Then:** Przycisk/opcja wyboru tej ścieżki jest nieaktywna (wyszarzona).
*   **Or:** System wyświetla komunikat błędu "Użytkownik już realizuje tę ścieżkę".
*   **And:** Nie wysyła się duplikat powiadomienia.

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

**Scenariusz Wyjątkowy: Błąd ładowania wideo**
*   **Given:** Próbuję otworzyć materiał wideo.
*   **When:** Występuje problem z połączeniem internetowym lub serwerem plików.
*   **Then:** Odtwarzacz wyświetla komunikat "Nie można załadować materiału. Sprawdź połączenie.".
*   **And:** Pojawia się przycisk "Spróbuj ponownie".
*   **And:** Postęp oglądania nie jest tracony (ostatnia znana pozycja jest zachowana lokalnie).

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

**Scenariusz Alternatywny: Niezaliczenie testu**
*   **Given:** Ukończyłem materiały i przystąpiłem do quizu.
*   **When:** Uzyskuję wynik < 80% (np. 65%).
*   **Then:** System wyświetla informację "Test niezaliczony. Spróbuj ponownie.".
*   **And:** Wskazuje sekcje materiału/wideo, które warto powtórzyć przed kolejną próbą.
*   **And:** Moduł pozostaje w statusie "W toku".

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

**Scenariusz Alternatywny: Brak danych do raportu**
*   **Given:** Wybrałem zakres dat (np. przyszły miesiąc) lub zespół, który nie rozpoczął szkoleń.
*   **When:** Klikam "Generuj Raport".
*   **Then:** System wyświetla komunikat "Brak danych dla wybranych kryteriów".
*   **And:** Nie generuje pustego pliku PDF/CSV.

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

**Scenariusz Alternatywny: Brak powtórek na dziś**
*   **Given:** Zalogowałem się do systemu.
*   **And:** Nie mam żadnych zaplanowanych powtórek na dzisiaj (wszystkie karty są "świeże" w pamięci).
*   **When:** Wchodzę w moduł "Asystent Powtórek".
*   **Then:** Wyświetla się komunikat "Wszystko na bieżąco! Wróć jutro.".
*   **And:** System proponuje opcjonalną naukę nowych materiałów.

### 4.7. Zarządzanie Wirtualnym Portfelem (US-9)

**Opis:** Umożliwia pracownikowi bieżący podgląd stanu posiadanych punktów oraz historii ich zdobywania za aktywność edukacyjną.  
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę mieć wgląd w saldo mojego portfela i historię transakcji,
*   aby wiedzieć, ile punktów zgromadziłem i na jakie benefity mogę je wymienić.

**Cel Biznesowy:** Budowanie motywacji do nauki poprzez transparentność systemu nagród i bezpośrednie powiązanie postępów z korzyściami.  
**Warunki Wstępne:** Użytkownik jest zalogowany do systemu.  
**Warunki Końcowe:** Użytkownik wyświetla aktualne saldo punktowe oraz listę operacji historycznych.

**Kryteria Akceptacji:**

**Scenariusz Główny: Podgląd salda i historii**
*   **Given:** Jestem zalogowanym pracownikiem i posiadałem wcześniej 100 pkt.
*   **And:** Właśnie ukończyłem quiz, za który otrzymałem 50 pkt.
*   **When:** Przechodzę do widoku "Mój Portfel".
*   **Then:** System wyświetla saldo równe 150 pkt.
*   **And:** Na liście transakcji widzę nową pozycję: "+50 pkt - Quiz: Podstawy Cloud" z dzisiejszą datą.


### 4.8. Realizacja Benefitów w Systemie Kafeteryjnym (US-10)

**Opis:** Moduł wymiany zgromadzonych punktów na usługi zewnętrzne (wellbeing, rozwój) poprzez automatyczną integrację z dostawcami.  
**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę samodzielnie wymieniać punkty na wybrane usługi prozdrowotne lub rozwojowe,
*   aby sfinansować mój wellbeing bez konieczności składania papierowych wniosków.

**Cel Biznesowy:** Zwiększenie utylizacji budżetu do poziomu 95% poprzez eliminację barier biurokratycznych w dostępie do świadczeń.  
**Warunki Wstępne:** Użytkownik posiada na koncie liczbę punktów równą lub wyższą niż cena wybranego benefitu.  
**Warunki Końcowe:** Saldo punktowe zostaje pomniejszone, a system generuje unikalny kod dostępu lub przesyła potwierdzenie do dostawcy.

**Kryteria Akceptacji:**

**Scenariusz Główny: Pomyślna wymiana punktów**
*   **Given:** Posiadam 500 pkt w portfelu.
*   **And:** Wybrałem benefit "Voucher do fizjoterapeuty" o wartości 400 pkt.
*   **When:** Klikam przycisk "Wymień punkty" i potwierdzam operację w oknie modalnym.
*   **Then:** Moje saldo zostaje natychmiast pomniejszone o 400 pkt (nowy stan: 100 pkt).
*   **And:** System wyświetla unikalny kod vouchera gotowy do użycia.
*   **And:** Otrzymuję e-mail z potwierdzeniem transakcji i instrukcją realizacji.

**Scenariusz Alternatywny: Niewystarczające saldo**
*   **Given:** Posiadam 100 pkt w portfelu.
*   **And:** Wybrałem benefit "Karta sportowa" o wartości 300 pkt.
*   **When:** Wyświetlam szczegóły tego benefitu.
*   **Then:** Przycisk "Wymień punkty" jest nieaktywny (wyszarzony).
*   **And:** Pod ceną widnieje komunikat: "Brakuje Ci 200 pkt, aby odebrać ten benefit".


### 4.9. Zarządzanie Ofertą Marketplace (US-11)

**Opis:** Panel administracyjny dla działu HR służący do konfigurowania katalogu nagród i zarządzania relacjami z dostawcami.  
**Historyjka Użytkownika:**
*   Jako HR Manager (Anna),
*   chcę dodawać nowe benefity do katalogu i określać ich wartość punktową,
*   aby oferta była atrakcyjna dla pracowników i optymalizowała wykorzystanie budżetu.

**Cel Biznesowy:** Efektywne zarządzanie budżetem szkoleniowo-benefitowym i dopasowanie oferty do realnych potrzeb pracowników.  
**Warunki Wstępne:** Użytkownik posiada uprawnienia Administratora lub HR Managera.  
**Warunki Końcowe:** Nowy benefit jest opublikowany i dostępny dla pracowników w katalogu Marketplace.

**Kryteria Akceptacji:**

**Scenariusz Główny: Dodanie nowego benefitu*
*   **Given:** Jestem zalogowana jako HR Manager i znajduję się w panelu zarządzania Marketplace.
*   **When:** Wypełniam formularz dodawania benefitu:  
    Nazwa ("Sesja z psychologiem"),  
    Cena (250 pkt),  
    Kategoria ("Wellbeing"),  
    Dostawca ("MindFull API").
*   **And:** Klikam "Opublikuj".
*   **Then:** Nowa oferta pojawia się na liście benefitów dostępnych dla wszystkich pracowników.


### 4.10. Monitoring Utylizacji Budżetu (US-12)

**Opis:** Moduł analityczny generujący raporty dotyczące wykorzystania środków finansowych w ramach platformy kafeteryjnej.  
**Historyjka Użytkownika:**
*   Jako HR Manager (Anna),
*   chcę generować raporty utylizacji budżetu w czasie rzeczywistym,
*   aby monitorować realizację celu 95% wykorzystania środków i reagować na odchylenia.

**Cel Biznesowy:** Kontrola kluczowych wskaźników efektywności (KPI) projektu oraz optymalizacja wydatków firmy.  
**Warunki Wstępne:** W systemie zarejestrowano aktywność użytkowników w module portfela.  
**Warunki Końcowe:** System generuje interaktywny raport finansowy lub plik eksportu z danymi o utylizacji budżetu.

**Kryteria Akceptacji:**

**Scenariusz Główny: Generowanie raportu**
*   **Given:** Jestem zalogowana jako HR Manager.
*   **When:** Przechodzę do sekcji "Raporty" i wybieram "Analiza wykorzystania budżetu".
*   **Then:** System wyświetla czytelny wykres porównujący sumę wydanych punktów z całkowitym budżetem rocznym.
*   **And:** Widzę wyliczony procent utylizacji (np. "Obecna utylizacja: 68%").
*   **And:** System sugeruje listę najmniej popularnych benefitów do ewentualnej wymiany.


### 4.11. Priorytetyzacja Wymagań

| ID | Funkcjonalność | Priorytet (MoSCoW) |
| :--- | :--- | :--- |
| US-1 | Przeglądanie Katalogu | **Must Have** |
| US-2 | Przypisywanie Ścieżek | **Must Have** |
| US-3 | Odtwarzacz Wideo | **Must Have** |
| US-4 | Weryfikacja Wiedzy | **Must Have** |
| US-9 | Zarządzanie Wirtualnym Portfelem | **Must Have** |
| US-10 | Realizacja Benefitów (Kafeteria) | **Must Have** |
| US-5 | Raportowanie Postępów | **Should Have** |
| US-7 | Asystent Powtórek | **Should Have** |
| US-11 | Zarządzanie Ofertą Marketplace | **Should Have** |
| US-12 | Monitoring Utylizacji Budżetu | **Should Have** |
| US-13 | Zarządzanie OKR (Objectives & Key Results) | **Must Have** |
| US-14 | Weryfikacja Długoterminowej Retencji Wiedzy | **Should Have** |
| US-15 | Personalizacja Algorytmu Powtórek | **Could Have** |

---

## 4.12. Zarządzanie OKR (US-13)

**Opis:** Moduł zarządzania celami OKR umożliwiający tworzenie, edycję, kaskadowanie oraz monitorowanie celów na poziomie strategicznym, zespołowym i indywidualnym. System zapewnia powiązanie celów z ścieżkami rozwoju, wizualizację drzewa celów oraz analitykę postępów, co wspiera kwartalną weryfikację realizacji strategii.

**Historyjki Użytkownika:**
*   Jako HR Manager / Administrator,
*   chcę tworzyć i edytować cele strategiczne i kluczowe rezultaty (KR),
*   aby zdefiniować priorytety organizacji i monitorować ich realizację.

*   Jako Manager,
*   chcę kaskadować cele do moich podwładnych i zespołów,
*   aby ich zadania były bezpośrednio powiązane z celami firmy.

*   Jako Pracownik,
*   chcę widzieć moje cele osobiste i ich powiązanie ze ścieżkami rozwoju,
*   aby lepiej ukierunkować naukę na realizację oczekiwań biznesowych.

**Cel Biznesowy:** Zapewnienie 100% transparentności powiązań między celami indywidualnymi a strategią firmy poprzez system kaskadowania OKR oraz umożliwienie kwartalnej weryfikacji realizacji strategii.

**Warunki Wstępne:** Użytkownik posiada odpowiednie uprawnienia (HR/Admin lub Manager). Istnieje co najmniej jedna zdefiniowana ścieżka rozwoju.

**Warunki Końcowe:** Cele są zdefiniowane, przypisane i powiązane z użytkownikami oraz ścieżkami; dostępna jest wizualizacja drzewa celów i raport kwartalny z postępami.

**Kryteria Akceptacji:**

**Scenariusz Główny: Utworzenie celu i powiązanie z KR**
*   **Given:** Jestem HR Managerem z uprawnieniami do tworzenia OKR.
*   **When:** Tworzę nowe Objective z jednym lub więcej Key Results i przypisuję właściciela oraz ramy czasowe.
*   **Then:** Cel pojawia się na liście OKR; każdy KR ma status i metryki śledzenia postępów.

**Scenariusz Główny: Kaskadowanie celu do zespołu**
*   **Given:** Istnieje Objective na poziomie strategicznym.
*   **When:** Manager kaskaduje Objective do zespołu, tworząc cele zespołowe i indywidualne powiązane z nadrzędnym Objective.
*   **Then:** System tworzy relacje rodzic-dziecko między celami, widoczne w wizualizacji drzewa oraz w profilach przypisanych użytkowników.

**Scenariusz Główny: Powiązanie ścieżki rozwoju z celem**
*   **Given:** Jest dostępna ścieżka rozwoju odpowiadająca kompetencjom wymaganym przez Objective.
*   **When:** HR lub Manager powiązuje Learning Path z Objective lub KR.
*   **Then:** Na dashboardzie użytkownika pojawia się informacja, które kursy wspierają realizację celu.

**Scenariusz Główny: Wizualizacja drzewa celów i raport kwartalny**
*   **Given:** Cele są zdefiniowane i powiązane z użytkownikami/ścieżkami.
*   **When:** HR generuje raport kwartalny lub otwiera widok drzewa celów.
*   **Then:** System pokazuje strukturę OKR, percentyl realizacji dla każdego celu oraz listę powiązanych ścieżek i użytkowników; raport zawiera wskaźnik zgodności powiązań (traceability) i metryki postępu.

**Scenariusz Alternatywny: Konflikt kaskadowania**
*   **Given:** Manager próbuje kaskadować Objective, który jest sprzeczny z istniejącymi priorytetami.
*   **When:** Próbuje przypisać cel o sprzecznych terminach lub priorytecie.
*   **Then:** System informuje o konflikcie i sugeruje konsultację z HR/Ownerem Objective.

**Kryteria Sukcesu:**
*   System umożliwia pełną śledzalność powiązań między celami strategicznymi, zespołowymi i indywidualnymi.
*   Wizualizacja drzewa celów wyświetla relacje i statusy w czytelny sposób.
*   Raport kwartalny dostarcza metryki wspierające weryfikację realizacji strategii.

## 4.13. Model danych OKR (hierarchia celów)

Poniżej propozycja podstawowego modelu danych obsługującego cele OKR, ich kaskadowanie, powiązania z użytkownikami oraz powiązania z Learning Paths.

1) `Objective`
* id: UUID (PK)
* title: string (255)
* description: text
* owner_id: UUID (FK -> User.id) — właściciel celu
* start_date: date
* end_date: date
* status: enum {draft, active, on_track, at_risk, completed, cancelled}
* progress_percent: decimal(5,2) — agregowany procent realizacji
* parent_id: UUID (FK -> Objective.id) nullable — relacja rodzic-dziecko
* created_at, updated_at: timestamps

2) `KeyResult`
* id: UUID (PK)
* objective_id: UUID (FK -> Objective.id)
* title: string (255)
* metric_type: enum {percentage, numeric, boolean, milestone}
* target_value: decimal/null
* current_value: decimal/null
* unit: string (np. "%", "items")
* owner_id: UUID (FK -> User.id)
* status: enum {not_started, in_progress, achieved, missed}
* start_date, end_date: date
* created_at, updated_at

3) `OKRAssignment` (przypisania celu do użytkownika/zespołu)
* id: UUID (PK)
* objective_id: UUID (FK)
* assignee_type: enum {user, team}
* assignee_id: UUID (FK -> User.id albo Team.id)
* role: enum {owner, contributor, reviewer}
* created_at

4) `ObjectiveLearningPath` (powiązanie Objective/KR z Learning Path)
* id: UUID (PK)
* objective_id: UUID (FK)
* learning_path_id: UUID (FK -> LearningPath.id)
* confidence: decimal (0..1) — jak silne jest powiązanie (optymalizacyjne)

5) `OKRProgressEvent` (historyczne zdarzenia / metryki)
* id: UUID (PK)
* key_result_id: UUID (FK nullable)
* objective_id: UUID (FK nullable)
* recorded_by: UUID (User.id)
* value: decimal
* note: text
* recorded_at: timestamp

6) `OKRAudit` (zmiany, kaskadowania, konflikty)
* id: UUID
* entity_type: string (Objective/KeyResult/Assignment)
* entity_id: UUID
* action: string (create/update/delete/cascade)
* performed_by: UUID
* details: json
* created_at: timestamp

Indeksowanie i spójność:
- Indeks na `Objective(parent_id)` dla szybkiego budowania drzewa.
- Indeks na `KeyResult(objective_id, owner_id)` dla raportów właściciela.
- Constraint: `Objective.end_date >= Objective.start_date`.
- Sumaryczny `Objective.progress_percent` może być wyliczany okresowo (batch) lub na żądanie przez agregację powiązanych KR.

Uwagi implementacyjne:
- Projekt wymusza hierarchiczną strukturę (rekurencyjne Objective z parent_id). Można rozważyć dodatkowe kolumny do materializowanej ścieżki (ltree / path) dla szybszych zapytań drzewa.
- Dla wysokiego obciążenia dashboardów rekomendowane są materializowane widoki/aggretacje (np. progress per objective) i warstwa cache (Redis).

Diagram (klasy, uproszczony):

```mermaid
classDiagram
    class Objective {
        +UUID id
        +String title
        +String description
        +UUID owner_id
        +Date start_date
        +Date end_date
        +Decimal progress_percent
        +UUID parent_id
    }

    class KeyResult {
        +UUID id
        +UUID objective_id
        +String title
        +Decimal target_value
        +Decimal current_value
        +String unit
    }

    class OKRAssignment {
        +UUID id
        +UUID objective_id
        +String assignee_type
        +UUID assignee_id
    }

    Objective "1" o-- "*" KeyResult : has
    Objective "1" o-- "*" Objective : children
    Objective "1" o-- "*" OKRAssignment : assigned
```

---

## 4.14. Weryfikacja Długoterminowej Retencji Wiedzy (US-14)

**Opis:** Moduł automatycznego testowania długoterminowej retencji wiedzy poprzez przeprowadzanie testów sprawdzających 30 dni po ukończeniu kursu. System mierzy rzeczywiste zapamiętanie materiału i dostarcza danych do analizy efektywności szkoleń.

**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę otrzymać test sprawdzający 30 dni po ukończeniu kursu,
*   aby zweryfikować, ile wiedzy faktycznie zapamiętałem i zidentyfikować obszary do powtórki.

*   Jako HR Manager,
*   chcę mieć dostęp do raportów retencji wiedzy w organizacji,
*   aby mierzyć rzeczywistą efektywność programów szkoleniowych i realizację celu 40% wzrostu retencji.

**Cel Biznesowy:** Zwiększenie wskaźnika retencji wiedzy o 40% w ciągu 6 miesięcy, mierzone testami sprawdzającymi przeprowadzanymi 30 dni po ukończeniu kursu.

**Warunki Wstępne:** Użytkownik ukończył kurs co najmniej 30 dni temu. System posiada zdefiniowane pytania do testu retencyjnego.

**Warunki Końcowe:** Wynik testu retencyjnego jest zapisany w profilu użytkownika i uwzględniony w raportach HR.

**Kryteria Akceptacji:**

**Scenariusz Główny: Automatyczne wyzwolenie testu retencyjnego**
*   **Given:** Ukończyłem kurs "Cloud Fundamentals" 30 dni temu.
*   **And:** Nie wykonałem jeszcze testu retencyjnego dla tego kursu.
*   **When:** Loguję się do systemu.
*   **Then:** System wyświetla powiadomienie "Czas na test retencyjny: Cloud Fundamentals".
*   **And:** Na dashboardzie pojawia się kafelek z testem do wykonania.

**Scenariusz Główny: Ukończenie testu retencyjnego**
*   **Given:** Przystąpiłem do testu retencyjnego dla kursu "Cloud Fundamentals".
*   **When:** Odpowiadam na wszystkie pytania i klikam "Zakończ test".
*   **Then:** System wyświetla wynik (np. "Zapamiętałeś 72% materiału").
*   **And:** System porównuje wynik z testem końcowym kursu i pokazuje różnicę (np. "Spadek o 8% względem wyniku końcowego").
*   **And:** System sugeruje konkretne moduły do powtórki na podstawie błędnych odpowiedzi.

**Scenariusz Alternatywny: Pominięcie testu retencyjnego**
*   **Given:** Otrzymałem powiadomienie o teście retencyjnym.
*   **When:** Klikam "Przypomnij później" lub ignoruję powiadomienie przez 7 dni.
*   **Then:** System wysyła przypomnienie e-mail.
*   **And:** Po 14 dniach nieaktywności test jest oznaczany jako "Pominięty" w raportach HR.

**Scenariusz Główny: Raport retencji dla HR**
*   **Given:** Jestem HR Managerem i chcę sprawdzić efektywność szkoleń.
*   **When:** Otwieram raport "Analiza Retencji Wiedzy" i wybieram okres ostatnich 6 miesięcy.
*   **Then:** System wyświetla średni wskaźnik retencji dla organizacji.
*   **And:** Pokazuje porównanie z poprzednim okresem (np. "Wzrost retencji o 35% względem poprzedniego kwartału").
*   **And:** Wskazuje kursy z najniższą retencją do przeglądu metodycznego.

---

## 4.15. Personalizacja Algorytmu Powtórek (US-15)

**Opis:** Moduł umożliwiający dostosowanie parametrów algorytmu Spaced Repetition do indywidualnych preferencji użytkownika oraz automatyczną adaptację na podstawie wyników uczenia.

**Historyjka Użytkownika:**
*   Jako pracownik,
*   chcę dostosować intensywność i częstotliwość powtórek do mojego stylu nauki,
*   aby system lepiej odpowiadał mojemu tempu przyswajania wiedzy.

*   Jako pracownik,
*   chcę, aby system automatycznie dostosowywał się do moich wyników,
*   aby trudniejsze dla mnie tematy pojawiały się częściej w powtórkach.

**Cel Biznesowy:** Wsparcie celu retencji wiedzy poprzez personalizację doświadczenia nauki i zwiększenie zaangażowania użytkowników w system powtórek.

**Warunki Wstępne:** Użytkownik ma aktywne sesje powtórkowe. System zebrał minimum 20 odpowiedzi użytkownika.

**Warunki Końcowe:** Parametry algorytmu są dostosowane do preferencji/wyników użytkownika.

**Kryteria Akceptacji:**

**Scenariusz Główny: Ręczna konfiguracja intensywności**
*   **Given:** Jestem w ustawieniach modułu "Asystent Powtórek".
*   **When:** Zmieniam intensywność powtórek z "Standardowa" na "Intensywna".
*   **Then:** System zwiększa liczbę codziennych pytań z 5 do 10.
*   **And:** Skraca interwały między powtórkami o 20%.
*   **And:** Wyświetla komunikat "Ustawienia zapisane. Nowa intensywność zostanie zastosowana od następnej sesji."

**Scenariusz Główny: Automatyczna adaptacja algorytmu**
*   **Given:** System zebrał 50 moich odpowiedzi z ostatnich 2 tygodni.
*   **And:** Mój wskaźnik poprawnych odpowiedzi dla kategorii "Kubernetes" wynosi 45%.
*   **When:** System przeprowadza analizę wyników (batch nocny).
*   **Then:** Pytania z kategorii "Kubernetes" są oznaczane jako "trudne" dla mojego profilu.
*   **And:** Interwały powtórek dla tych pytań są automatycznie skracane.
*   **And:** Otrzymuję sugestię "Rozważ powtórkę materiału: Kubernetes Basics" na dashboardzie.

**Scenariusz Alternatywny: Reset do ustawień domyślnych**
*   **Given:** Zmieniłem ustawienia algorytmu powtórek.
*   **And:** Chcę wrócić do ustawień rekomendowanych przez system.
*   **When:** Klikam "Przywróć domyślne" w ustawieniach.
*   **Then:** System resetuje wszystkie parametry do wartości bazowych.
*   **And:** Historia adaptacji algorytmu jest zachowana do celów analitycznych.

## 5. Atrybuty Jakościowe

### 5.1. Jakość wykonania

*   **Wydajność (Performance):**
    *   **WNF-WYD-01:** Czas ładowania strony głównej katalogu nie może przekroczyć 1.5 sekundy przy 200 jednoczesnych użytkownikach (mierzone medianą z 1-minutowych okien pomiarowych).
    *   **WNF-WYD-02:** Buforowanie wideo musi rozpocząć się w ciągu 2 sekund od kliknięcia "Odtwórz" w 95% przypadków dla połączeń o przepustowości >= 5 Mbps.
    *   **WNF-WYD-03:** Czas odpowiedzi integracji z API zewnętrznego dostawcy (np. generowanie kodu vouchera) nie może przekroczyć 2.0 sekund w 95% zapytań przy obciążeniu do 50 zapytań na sekundę.
    *   **WNF-WYD-04:** Operacja zapisu transakcji w portfelu (debet/kredyt) powinna zakończyć się w czasie <= 500 ms w 99% przypadków.

*   **Dostępność (Availability):**
    *   **WNF-NIEZ-01:** Całkowita dostępność systemu musi wynosić >= 99.8% w skali roku (SLA), z wyłączeniem zaplanowanych okien serwisowych.
    *   **WNF-NIEZ-02:** Krytyczne moduły (Marketplace, Portfel) muszą być dostępne >= 99.9% w skali miesiąca.
    *   **WNF-NIEZ-03:** Kopie zapasowe: dopuszczalna utrata danych (RPO) <= 1 godzina; czas odtworzenia systemu (RTO) <= 4 godziny.

*   **Bezpieczeństwo (Security):**
    *   **WNF-BEZ-01:** Hasła muszą być hashowane algorytmem `bcrypt` z solą; parametry cost >= 12.
    *   **WNF-BEZ-02:** Sesje użytkowników wygasają po 30 minutach nieaktywności; odświeżenie tokenu wymaga ponownej walidacji MFA dla krytycznych operacji.
    *   **WNF-BEZ-03:** Dostęp do panelu HR wymaga uwierzytelniania wieloskładnikowego (MFA) i audytowania wszystkich operacji administracyjnych.
    *   **WNF-BEZ-04:** Każda operacja zmiany salda w portfelu musi być zapisana w niezmiennym dzienniku audytu zawierającym: ID transakcji, ID użytkownika, timestamp (ms), typ operacji i sumę kontrolną; logi audytu przechowywane minimum 2 lata.
    *   **WNF-BEZ-05:** Dane w raportach agregowanych muszą być anonimizowane; dostęp do surowych danych PII ograniczony do ról HR/Admin i rejestrowany w logach dostępu.

*   **Skalowalność (Scalability):**
    *   **WNF-SKAL-01:** System musi być horyzontalnie skalowalny i obsługiwać do 5000 jednoczesnych sesji przy zachowaniu WNF-WYD-01.
    *   **WNF-SKAL-02:** Warstwa transakcyjna portfela musi obsłużyć do 150 operacji/s przez 10 minut (peak) z sukcesem >= 99% bez utraty spójności.

### 5.2. Jakość projektu

*   **Modyfikowalność (Modifiability):**
    *   **WNF-ROZ-01:** Możliwość dodania nowego typu pytania w module Quiz bez zmiany schematu bazy danych lub przestoju systemu; walidacja: dodanie i wdrożenie nowego typu nie wymaga migracji bazy danych w > 95% przypadków.
    *   **WNF-ROZ-02:** Nowa integracja z dostawcą zewnętrznym musi być możliwa poprzez implementację adaptera (plugin) bez modyfikacji kodu Core; integracja powinna przejść testy integracyjne automatycznie i mieć pokrycie testami >= 80% dla ścieżek krytycznych.

*   **Przenośność (Portability):**
    *   **WNF-PRZEN-01:** Aplikacja (Frontend, Backend, Baza) musi być konteneryzowalna i uruchamialna za pomocą `docker-compose up` na maszynie deweloperskiej w czasie <= 2 minut (cold start).
    *   **WNF-PRZEN-02:** Wszystkie konfiguracje środowiskowe (klucze API, endpointy, certyfikaty) muszą być zarządzane przez zmienne środowiskowe; zmiana dostawcy nie wymaga przebudowy obrazu kontenera.

*   **Obserwowalność i Utrzymanie (Observability & Maintainability):**
    *   **WNF-OBS-01:** System musi emitować metryki (latency histogramy, error rate, throughput) dla kluczowych endpointów; dane metryk agregowane są przez co najmniej 90 dni.
    *   **WNF-OBS-02:** Centralne logowanie z poziomami TRACE/DEBUG/INFO/WARN/ERROR oraz możliwość korelacji logów po `request_id`/`transaction_id`.
    *   **WNF-OBS-03:** Alerty krytyczne (np. spadek dostępności poniżej SLA, wzrost błędów >1% w 5-min oknie) muszą generować powiadomienia do kanału operacyjnego (e-mail/Slack) z czasem reakcji SLA 1 godzina.

### 5.3. Priorytetyzacja Atrybutów Jakościowych
1.  **Krytyczne:** Bezpieczeństwo danych (RODO) i Wydajność (Odtwarzanie wideo). Bezpieczeństwo transakcji.
2.  **Wysokie:** Dostępność systemu. Wydajność API.
3.  **Średnie:** Modyfikowalność i Przenośność.

---

## 6. Odkrywanie i Analiza Wymagań

### 6.1. Analiza Porównawcza (Benchmarking)

**Konkurencja:**
*   **Udemy for Business:** Popularna platforma z kursami wideo.
*   **Pluralsight:** Platforma skoncentrowana na umiejętnościach technicznych.
*   **MyBenefit, Medicover Benefits:** Platformy skupione wyłącznie na świadczeniach pozapłacowych, bez powiązania z rozwojem kompetencji.


**Kryteria Oceny:**
1.  **Materiały Wewnętrzne:** Czy można hostować własne wideo?
2.  **Spaced Repetition:** Czy system wspiera inteligentne powtórki?
3.  **Koszt:** Model rozliczeń.
4.  **System Benefitowy i Wellbeing:** Czy system pozwala na elastyczną wymianę punktów na usługi prozdrowotne i rozwojowe?

**Synteza Wyników:**
*   **Udemy/Pluralsight:** Oferują świetne materiały ogólne, ale brakuje im wsparcia dla specyficznych procesów firmowych i hostingu tajnych materiałów wewnętrznych. Żadna z nich nie posiada wbudowanego modułu Active Recall/Spaced Repetition w standardzie.
*   **Intelligent LMS:** Wypełnia niszę poprzez połączenie własnych treści (Internal Knowledge) z nowoczesnymi metodami nauki (SR/Active Recall), co jest kluczowe dla ROI.
*   **MyBenefit/Kafeterie:** Skupiają się wyłącznie na katalogu nagród. Brak integracji z procesem szkoleniowym sprawia, że nie wspierają aktywnie rozwoju kompetencji pracowników.

---

## 7. Dodatki

### Dodatek A: Modele Analityczne
*   **Diagram Przypadków Użycia (Use Case):**

```mermaid
flowchart LR
    %% Aktorzy
    emp("👤 Pracownik")
    mgr("👤 Manager Zespołu")
    hr("👤 HR Manager")
    prov("⚙️ Dostawca Benefitów (API)")

    %% Granica Systemu
    subgraph "Intelligent LMS & Benefit Hub"
        direction TB
        UC1(["Przeglądaj Katalog (US-1)"])
        UC2(["Realizuj Naukę / Quizy (US-4)"])
        UC3(["Sprawdź Portfel (US-9)"])
        UC4(["Wymień Punkty na Benefit (US-10)"])
        UC5(["Przypisz Ścieżkę (US-2)"])
        UC6(["Zarządzaj Ofertą (US-11)"])
        UC7(["Raportuj Utylizację (US-12)"])
    end

    %% Relacje
    emp --> UC1
    emp --> UC2
    emp --> UC3
    emp --> UC4
    
    UC2 -.->|include| UC3
    UC4 <--> prov

    mgr --> UC5
    mgr -.->|dziedziczy| emp

    hr --> UC6
    hr --> UC7
```

*   **Diagram Klas:**

```mermaid
classDiagram
    class User {
        +int id
        +String email
        +login()
    }

    class Employee {
        +Wallet wallet
        +redeemBenefit()
    }

    class Wallet {
        +int balance
        +List~Transaction~ history
        +addPoints(amount)
        +deductPoints(amount)
    }

    class Transaction {
        +int id
        +DateTime timestamp
        +int amount
        +String type
    }

    class Benefit {
        +int id
        +String name
        +int pointCost
        +String providerId
    }

    class Quiz {
        +int rewardPoints
        +complete()
    }

    User <|-- Employee
    Employee "1" -- "1" Wallet
    Wallet "1" *-- "*" Transaction
    Transaction "*" -- "0..1" Benefit : dotyczy
    Quiz "1" -- "1" Transaction : generuje
```

### Dodatek B: Persony Użytkowników
Szczegółowe karty person (Anna i Piotr) znajdują się w pliku [personas.md](personas.md).

### Dodatek C: Kwestie do Rozwiązania
1.  Wybór dostawcy hostingu wideo (Vimeo Pro vs AWS S3).
2.  Decyzja o frameworku frontendowym (Angular vs React - zespół preferuje Angular).
3.  Wycena Punktowa i Atrakcyjność: Opracowanie algorytmu przeliczania trudności kursu na wartość punktową. Algorytm musi balansować między "sprawiedliwością" a "atrakcyjnością" nagród – zbyt wysokie progi punktowe mogą zniechęcić użytkowników i uniemożliwić osiągnięcie celu 95% utylizacji budżetu.
4. Wybór Standardu API: Decyzja o wyborze wiodącego dostawcy platformy benefitowej (np. Medicover, MyBenefit) pod kątem stabilności ich API i łatwości generowania kodów w czasie rzeczywistym.
