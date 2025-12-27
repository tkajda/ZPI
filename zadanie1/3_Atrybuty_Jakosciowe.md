# 3. Specyfikacja atrybutów jakościowych

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
