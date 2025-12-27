# 4. Ograniczenia i założenia projektowe

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
