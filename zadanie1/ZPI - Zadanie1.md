# Analiza i specyfikacja driverów architektonicznych

## Cel zadania

Twoim zadaniem jest przeprowadzenie analizy i przygotowanie dokumentu opisującego drivery architektoniczne dla Twojego projektu. Celem jest wykazanie zrozumienia, w jaki sposób potrzeby biznesowe i wymagania, ograniczenia i ryzykowne założenia, przekładają się na konkretne decyzje architektoniczne.

**Uwaga:** Praca jest w całości **indywidualna**. Projekt realizowany jest grupowo, jednak to zadanie każdy student wykonuje samodzielnie. Wymagana jest jedynie koordynacja wewnątrz zespołu w celu wyboru **różnych, istotnie odmiennych celów biznesowych** dla każdego członka grupy. Każdy student opracowuje własną wizję, wymagania i architekturę dla wybranego przez siebie celu, aby uniknąć powielania treści. Nie dopuszcza się kopiowania fragmentów pracy między członkami zespołu.

## Struktura dokumentu

Twój dokument powinien składać się z poniższych sekcji, które razem tworzą spójny obraz driverów architektonicznych projektu.

### 1. Wizja i zakres projektu

Ta sekcja stanowi uzasadnienie istnienia projektu i odpowiada na pytanie "Dlaczego tworzymy ten produkt?". Zamiast skupiać się na pojedynczym celu, opisz szerszy kontekst biznesowy.

#### Problem biznesowy i szanse rynkowe:

- Opisz szczegółowo, jaki problem rozwiązuje tworzony produkt. Kim są osoby lub organizacje, które go będą wykorzystywać? Jakie są ich problemy?
- Jaką wartość biznesową lub społeczną adresuje projekt? Czy wypełnia niszę na rynku, usprawnia istniejący proces, czy tworzy nową możliwość?

#### Wizja produktu:

Sformułuj jedno lub dwa zdania, które opisują nadrzędny cel i przyszły stan produktu. Wizja powinna być inspirująca i stanowić "gwiazdę polarną" dla zespołu.

**Przykład:** 
- "Komputer na każdym biurku i w każdym domu."  
- "Zapewnienie dostępu do informacji ze świata za pomocą jednego kliknięcia."

#### Główny cel biznesowy (zgodny ze SMART):

Wybierz i opisz jeden najważniejszy cel biznesowy, który projekt ma zrealizować w pierwszej kolejności. Upewnij się, że jest szczegółowy, mierzalny, osiągalny, realistyczny i terminowy.

**Przykład:** "W ciągu 6 miesięcy od uruchomienia wersji MVP, osiągnięcie 1000 aktywnych wolontariuszy, co przełoży się na realizację co najmniej 50 projektów społecznych i zwiększenie zaangażowania społeczności, budując tym samym podstawy dla zrównoważonego rozwoju platformy i pozyskania 3 nowych partnerów strategicznych."

#### Kluczowe metryki sukcesu (KPIs):

Zdefiniuj 2-3 mierzalne wskaźniki (KPIs), które pozwolą ocenić, czy główny cel biznesowy został osiągnięty.

**Przykłady do celu powyżej:**
1. Liczba aktywnych wolontariuszy w ciągu 6 miesięcy od uruchomienia MVP > 1000.
2. Liczba zrealizowanych projektów społecznych w ciągu 6 miesięcy od uruchomienia MVP > 50.
3. Liczba pozyskanych partnerów strategicznych w ciągu 6 miesięcy od uruchomienia MVP > 3.

#### Główne klasy użytkowników i interesariusze:

- Zidentyfikuj kluczowe grupy użytkowników oraz innych ważnych interesariuszy (np. sponsorzy, partnerzy).
- Dla najważniejszych klas użytkowników stwórz persony. Persona to fikcyjna postać reprezentująca grupę, posiadająca imię, cele i frustracje. Pomaga to wczuć się w potrzeby użytkownika i projektować z jego perspektywy.

**Przykład persony:** "Anna, 21-letnia studentka dążąca do zdobycia pierwszego doświadczenia zawodowego. Chce szybko znaleźć wolontariat zgodny z jej zainteresowaniami, ale frustruje ją konieczność przeszukiwania wielu niespójnych stron."

### 2. Kluczowe wymagania i priorytetyzacja dla MVP

W tej sekcji określisz zakres produktu w wersji MVP (Minimum Viable Product), który jest niezbędny do realizacji głównego celu biznesowego. Wymagania funkcjonalne opisują, co system ma robić.

#### Wymagania użytkownika (Historyjki użytkownika):

Wypisz kluczowe wymagania z perspektywy użytkownika w formie historyjek użytkownika (User Stories).

**Format:** "Jako [persona/typ użytkownika], chcę [wykonać akcję], aby [osiągnąć cel/korzyść]."

**Przykład:** "Jako koordynator w NGO (non-governmental organization), chcę opublikować nową ofertę wolontariatu w mniej niż 5 minut, aby szybko dotrzeć do potencjalnych kandydatów."

#### Priorytetyzacja wymagań dla MVP:

Podejmowanie decyzji o zakresie MVP nie powinno być arbitralne. Aby dokonać obiektywnego wyboru, zastosuj model priorytetyzacji, oparty na wartości, koszcie i ryzyku.

Stwórz tabelę dla 5-7 kandydujących funkcji/historyjek. Dla każdej z nich oszacuj (w skali Fibonacciego: 1, 2, 3, 5, 8, 13, 21):

- **Korzyść:** Jak dużą korzyść przyniesie użytkownikowi ta funkcja?
- **Kara:** Jak dużą stratę poniesie użytkownik lub biznes, jeśli funkcja zostanie pominięta? (np. utrata klientów, kary umowne, niemożność wykonania kluczowego zadania).
- **Koszt:** Względny koszt implementacji (szacowany przez zespół).
- **Ryzyko:** Względne ryzyko techniczne implementacji (złożoność, niepewność).

Oblicz priorytet dla każdej funkcji, używając wzoru, który równoważy te czynniki. Funkcje o najwyższym priorytecie są najlepszymi kandydatami do MVP. Uzasadnij swój wybór zakresu MVP w oparciu o wyniki tej analizy.

**Sposób obliczania priorytetu:**

Priorytet można obliczyć, sumując Korzyść i Karę (reprezentujące wartość dla użytkownika), a następnie dzieląc tę sumę przez sumę Kosztu i Ryzyka (reprezentujące wysiłek i niepewność).

`Priorytet = (Korzyść + Kara) / (Koszt + Ryzyko)`

Im wyższa wartość priorytetu, tym dana funkcja jest bardziej wartościowa w stosunku do wysiłku i ryzyka, co czyni ją lepszym kandydatem do MVP.

### 3. Specyfikacja atrybutów jakościowych za pomocą scenariuszy

Atrybuty jakościowe (nazywane też wymaganiami niefunkcjonalnymi) definiują, jak dobrze system ma działać, w przeciwieństwie do wymagań funkcjonalnych, które określają, co system ma robić. Są one kluczowymi driverami architektonicznymi, ponieważ decyzje podjęte w celu ich spełnienia mają fundamentalny wpływ na strukturę, technologię i koszt systemu.

Często pozostają one w konflikcie (np. wysokie bezpieczeństwo może negatywnie wpłynąć na wydajność), dlatego ich świadomy wybór i precyzyjna specyfikacja są kluczowe. Abstrakcyjne stwierdzenia, takie jak "system ma być szybki i bezpieczny", są bezużyteczne z inżynierskiego punktu widzenia, ponieważ nie da się zmierzyć ich realizacji.

#### **Krok 1: Wybór i priorytetyzacja atrybutów**

Wybierz 5-7 najważniejszych atrybutów jakościowych dla Twojego systemu. Aby ułatwić wybór, możesz skorzystać z poniższej listy popularnych atrybutów:

**Przykłady:**
| Kategoria | Atrybut Jakościowy | Opis |
| :--- | :--- | :--- |
| **Jakość wykonania** | **Wydajność** (Performance) | Jak szybko system odpowiada na żądania w określonych warunkach? |
| | **Dostępność** (Availability) | Jak często system jest dostępny i działa poprawnie? (np. 99.9% czasu) |
| | **Bezpieczeństwo** (Security) | Jak system chroni dane przed nieautoryzowanym dostępem lub atakiem? |
| | **Skalowalność** (Scalability) | Jak system radzi sobie ze wzrostem obciążenia (np. liczby użytkowników, danych)? |
| **Jakość projektu** | **Modyfikowalność** (Modifiability) | Jak łatwo i tanio można wprowadzać zmiany w systemie w przyszłości? |
| | **Testowalność** (Testability) | Jak łatwo można zweryfikować, czy system działa poprawnie? |
| | **Przenośność** (Portability) | Jak łatwo można przenieść system na inne środowisko (np. inny system operacyjny, chmurę)? |

Ustaw wybrane atrybuty w kolejności od najważniejszego do najmniej ważnego i **uzasadnij swój wybór** w kontekście głównego celu biznesowego Twojego projektu.

#### **Krok 2: Mierzalna specyfikacja (dla TOP 3 atrybutów)**

Dla trzech najwyżej spriorytetyzowanych atrybutów stwórz mierzalną specyfikację w formie **scenariusza jakościowego**. Scenariusz ten precyzuje, co dokładnie oznacza dany atrybut w kontekście Twojego systemu, unikając niejasności. Użyj schematu składającego się z 6 elementów:


| Element           | Opis                                                                                             |
| :---------------- | :----------------------------------------------------------------------------------------------- |
| **Źródło bodźca** | Kto lub co generuje zdarzenie? (np. użytkownik, system zewnętrzny, administrator).                |
| **Bodziec**       | Co się dzieje? Jakie zdarzenie następuje? (np. żądanie wyświetlenia strony, awaria serwera, atak DDoS). |
| **Artefakt**      | Której części systemu to dotyczy? (np. cały system, baza danych, interfejs użytkownika).         |
| **Środowisko**    | W jakich warunkach działa system w momencie zdarzenia?                                           |
| **Reakcja**       | Co system powinien zrobić w odpowiedzi na bodziec?                                               |
| **Miara reakcji** | Jak zmierzymy sukces reakcji? Musi to być konkretna, mierzalna wartość.                          |

---

**Przykład: Scenariusz dla atrybutu "Wydajność"**

| Element           | Opis                                                                                             |
| :---------------- | :----------------------------------------------------------------------------------------------- |
| **Źródło bodźca** | Użytkownik końcowy.                                                                              |
| **Bodziec**       | Inicjuje wyszukiwanie ofert wolontariatu z użyciem trzech filtrów.                               |
| **Artefakt**      | Moduł wyszukiwania i baza danych ofert.                                                          |
| **Środowisko**    | Szczytowe obciążenie systemu (zdefiniowane jako 1000 jednoczesnych użytkowników wykonujących różne akcje). |
| **Reakcja**       | System przetwarza zapytanie, filtruje wyniki i wyświetla pierwszą stronę pasujących ofert.       |
| **Miara reakcji** | Czas od wysłania żądania do wyświetlenia wyników jest **krótszy niż 1.5 sekundy dla 95% zapytań**. |

---

#### **Krok 3: Analiza kompromisów architektonicznych**

Dla każdego z trzech zdefiniowanych scenariuszy opisz, jakie kompromisy architektoniczne mogą być konieczne do ich osiągnięcia. Pamiętaj, że nie ma "darmowych" rozwiązań – poprawa jednego atrybutu często odbywa się kosztem innego.

**Przykład analizy kompromisu dla scenariusza "Wydajność":**

*   **Cel:** Osiągnięcie czasu odpowiedzi poniżej 1.5 sekundy.
*   **Możliwe rozwiązanie architektoniczne:** Wprowadzenie zaawansowanego mechanizmu cache (np. Redis) do przechowywania wyników często wyszukiwanych fraz.
*   **Kompromis:**
    *   **Pozytywny:** Znacząco poprawiamy **wydajność** dla powtarzalnych zapytań.
    *   **Negatywny:**
        *   Pogarszamy **modyfikowalność**, ponieważ logika systemu staje się bardziej złożona (trzeba zarządzać unieważnianiem cache).
        *   Zwiększamy **koszt operacyjny** poprzez konieczność utrzymania dodatkowej usługi (Redis).
        *   Wprowadzamy ryzyko wyświetlania **nieaktualnych danych**, jeśli mechanizm unieważniania cache zawiedzie.

### **4. Ograniczenia i założenia projektowe**

Zgodnie z metodyką inżynierii wymagań, kluczowe jest świadome rozróżnienie między **ograniczeniami** (twardymi ramami, które zawężają pole decyzji) a **założeniami** (ryzykownymi hipotezami). Oba te elementy mają fundamentalny wpływ na architekturę, ale zarządzamy nimi w zupełnie inny sposób.

Ograniczenia to decyzje lub warunki, które są nam narzucone i nie podlegają negocjacjom. Zamiast z nimi walczyć, architekt musi je zaakceptować i projektować system *w ich ramach*. Ignorowanie ograniczeń prowadzi do rozwiązań, które są niemożliwe do wdrożenia w danym kontekście.

**Przykład 1: Ograniczenie technologiczne**

*   **Ograniczenie:** System musi być wdrożony na firmowej infrastrukturze opartej o klaster Kubernetes w wersji X.
*   **Źródło:** Polityka działu IT firmy, która standaryzuje wykorzystywaną technologię w celu obniżenia kosztów utrzymania.
*   **Wpływ na architekturę:**
    *   Wyklucza to możliwość użycia specyficznych, zarządzanych usług "serverless" (np. AWS Lambda, Google Cloud Functions) jako głównego modelu obliczeniowego.
    *   Wymusza projektowanie aplikacji w postaci skonteneryzowanych mikroserwisów lub monolitu, które można uruchomić na klastrze K8s.
    *   Narzuca konieczność stworzenia definicji wdrożeń (np. pliki YAML dla Helm/Kustomize) zgodnych ze standardami firmowymi.

**Przykład 2: Ograniczenie biznesowe**

*   **Ograniczenie:** Całkowity budżet na utrzymanie infrastruktury wersji MVP nie może przekroczyć 1000 PLN miesięcznie przez pierwsze 6 miesięcy.
*   **Źródło:** Sponsor projektu, który chce zminimalizować początkowe ryzyko finansowe.
*   **Wpływ na architekturę:**
    *   Konieczność wyboru dostawcy chmury i usług, które ofertuje tani hosting przez krótki okres.
    *   Wymusza projektowanie z myślą o optymalizacji kosztów: użycie mniejszych maszyn, automatyczne skalowanie do zera w nocy, wybór tańszych typów storage'u.
    *   Wyklucza na starcie drogie, wysoko dostępne konfiguracje multi-region, które można będzie wprowadzić później, po walidacji modelu biznesowego.
    * Rozpoczęcie implementacji może okazać się możliwe jedynie bez wykorzystania bazy danych w początkowych fazach, w celu redukcji kosztów.

**Przykład 3: Ograniczenie prawne**

*   **Ograniczenie:** System musi być zgodny z Rozporządzeniem o Ochronie Danych Osobowych (RODO), a wszystkie dane osobowe wolontariuszy muszą być fizycznie przechowywane na serwerach zlokalizowanych w granicach Europejskiego Obszaru Gospodarczego (EOG).
*   **Źródło:** Prawo Unii Europejskiej.
*   **Wpływ na architekturę:**
    *   Drastycznie zawęża wybór dostawców usług chmurowych do tych, którzy posiadają centra danych w EOG.
    *   Wymusza implementację mechanizmów do obsługi praw użytkowników (prawo do bycia zapomnianym, prawo do eksportu danych), co musi być uwzględnione w projekcie bazy danych i API.
    *   Narzuca konieczność anonimizacji danych w środowiskach deweloperskich i testowych.

---

#### **4.2. Założenia projektowe**

Założenia to stwierdzenia, które przyjmujemy za prawdziwe, aby móc kontynuować pracę, mimo braku 100% pewności. Każde założenie to ukryte ryzyko. Profesjonalne zarządzanie wymaganiami polega na identyfikacji tych założeń, ocenie ryzyka i zaplanowaniu ich weryfikacji.

**Identyfikacja i analiza założeń:**

*   Wskaż co najmniej dwa kluczowe założenia, które przyjmiesz w projekcie.
*   Dla każdego założenia opisz jego **treść**, **ryzyko** (co się stanie, jeśli okaże się fałszywe?) oraz **plan walidacji** (jak, kiedy i kto sprawdzi, czy założenie jest prawdziwe?).

**Przykład 1: Założenie techniczne**

*   **Założenie:** Zakładamy, że zewnętrzne, darmowe API do geolokalizacji (GeoAPI) będzie w stanie obsłużyć do 500 zapytań na minutę, co jest naszą estymacją dla szczytowego obciążenia.
*   **Ryzyko:** Jeśli API jest wolniejsze lub ma niższy limit, kluczowa funkcja wyszukiwania ofert "w mojej okolicy" przestanie działać pod obciążeniem, co spowoduje frustrację użytkowników i porzucenie aplikacji.
*   **Plan walidacji:**
    *   **Co:** Przeprowadzenie testów obciążeniowych na GeoAPI.
    *   **Jak:** Stworzenie prostego skryptu testowego, który będzie wysyłał zapytania do API ze stopniowo rosnącą częstotliwością.
    *   **Kiedy:** W pierwszym sprincie, zanim rozpoczniemy implementację logiki biznesowej zależnej od tego API.
    *   **Kto:** Jeden z deweloperów.

**Przykład 2: Założenie dotyczące użytkownika lub biznesu**

*   **Założenie:** Zakładamy, że koordynatorzy z organizacji NGO będą chętni poświęcić około 15 minut na wypełnienie szczegółowego formularza opisującego nową ofertę wolontariatu.
*   **Ryzyko:** Jeśli proces ten okaże się dla nich zbyt długi lub uciążliwy, będą porzucać formularz w połowie, a nasza platforma nie będzie miała wystarczającej liczby ofert, aby przyciągnąć wolontariuszy. Cały model biznesowy zawiedzie.
*   **Plan walidacji:**
    *   **Co:** Testy użyteczności prototypu formularza.
    *   **Jak:** Stworzenie klikalnego prototypu formularza w narzędziu typu Figma i poproszenie 5-7 prawdziwych koordynatorów z zaprzyjaźnionych NGO o jego "wypełnienie" w ramach sesji z moderatorem.
    *   **Kiedy:** Przed rozpoczęciem implementacji backendu i frontend-u formularza.
    *   **Kto:** UX Designer lub Product Owner.
    
---

## Forma i sposób oddania

- **Format:** Dokument PDF.
- **Oznaczenie:** Wyraźnie oznacz każdą powyżej kategorii.
- **Termin:** 7.12.2025.
- **Tytuł e-maila:** "ZPI – Drivery architektoniczne – Imię i Nazwisko" **Uwaga:** Błędny tytuł przekieruje zadanie do spamu.
- **Ocena:** Przygotowana dokumentacja będzie jedną ze składowych oceny końcowej podczas obrony projektu.


**## Kryteria oceny**

Praca będzie oceniana pod kątem merytorycznym, analitycznym oraz formalnym. Maksymalna liczba punktów do zdobycia wynosi **50**. Ocena końcowa będzie sumą punktów uzyskanych z poszczególnych sekcji, które odzwierciedlają kluczowe umiejętności w zakresie inżynierii wymagań i myślenia architektonicznego.

| **Sekcja** | **Elementy podlegające ocenie** | **Maks. punkty** | **Opis kryterium** |
| :--- | :--- | :--- | :--- |
| **1. Wizja i zakres projektu** | 1.1. Problem, wizja i cel SMART<br>1.2. KPIs<br>1.3. Persony i interesariusze | **10** | Oceniana będzie klarowność opisu problemu, spójność wizji z celem, poprawność sformułowania celu w metodyce SMART oraz jego powiązanie z mierzalnymi wskaźnikami sukcesu (KPIs). Ważna jest również głębia i trafność stworzonych person. |
| **2. Wymagania i priorytetyzacja MVP** | 2.1. Historyjki użytkownika<br>2.2. Tabela priorytetyzacji<br>2.3. Uzasadnienie zakresu MVP | **10** | Sprawdzana będzie umiejętność tworzenia poprawnych historyjek użytkownika, logiczne zastosowanie modelu priorytetyzacji (nie tylko wypełnienie tabeli, ale sensowne oszacowanie wartości) oraz przekonujące uzasadnienie wyboru funkcji do MVP w oparciu o wyniki analizy. |
| **3. Atrybuty jakościowe** | 3.1. Wybór i uzasadnienie atrybutów<br>3.2. Mierzalne scenariusze jakościowe<br>3.3. Analiza kompromisów | **12** | Najwyżej punktowana sekcja. Kluczowe jest powiązanie wyboru atrybutów z celem biznesowym, a przede wszystkim **stworzenie precyzyjnych i mierzalnych (testowalnych) scenariuszy jakościowych**. Oceniana będzie również świadomość i analiza potencjalnych kompromisów architektonicznych. |
| **4. Ograniczenia i założenia** | 4.1. Analiza ograniczeń<br>4.2. Analiza założeń | **10** | Oceniana będzie umiejętność poprawnego rozróżnienia między ograniczeniami a założeniami. W przypadku ograniczeń kluczowy jest opis ich bezpośredniego wpływu na architekturę. W przypadku założeń – identyfikacja realnego ryzyka oraz przedstawienie konkretnego, wykonalnego planu walidacji. |
| **5. Jakość ogólna i spójność** | 5.1. Struktura, format, język<br>5.2. Głębia analizy i indywidualny wkład | **8** | Oceniana będzie ogólna jakość dokumentu: jego przejrzystość, profesjonalizm, poprawność językowa oraz estetyka. Dodatkowe punkty przyznawane są za głębię analizy, wykazanie zrozumienia powiązań między sekcjami oraz przedstawienie własnych, unikalnych przemyśleń wykraczających poza proste wypełnienie szablonu. |
| **Suma** | | **50** | |

## Źródła
- [Wiegers K. - Specyfikacja oprogramowania. Inżynieria wymagań Wydanie III.pdf](https://helion.pl/ksiazki/specyfikacja-oprogramowania-inzynieria-wymagan-wydanie-iii-karl-wiegers-joy-beatty,speo3v.htm?srsltid=AfmBOoozqePGdHY3BKcUIbpVuo5nTT3uJ_MkCJeonulGOoUyIcTqXj1h#format/e)










