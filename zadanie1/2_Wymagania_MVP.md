# 2. Kluczowe wymagania i priorytetyzacja dla MVP

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
