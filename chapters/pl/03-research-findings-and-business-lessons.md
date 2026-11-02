## 3. Wyniki rozpoznania i wnioski dla firmy

Wcześniejsze rozpoznanie wskazało kilka sposobów utraty kontroli nad informacjami przy korzystaniu z AI. Ten rozdział zbiera ustalenia dotyczące OpenAI jako podstawę dalszej analizy nadzoru. Ujawnienie przez pracownika, awaria po stronie dostawcy i podejrzenie wtórnego wykorzystania know-how wymagają różnych dowodów oraz zabezpieczeń. Nie należy przedstawiać ich jako równoważnych przykładów kradzieży danych.

**Stan rozpoznania:** Źródła sprawdzono ponownie 2 listopada 2026 r. Poniżej rozróżniono doniesienia prasowe, relacje uczestników, ustalenia dostawcy i orzeczenie sądu. Wymagania biznesowe są proponowanymi wnioskami z analizy.

### 3.1 Doniesienia o ujawnieniu przez pracowników: Samsung, 2023

Cybersecurity Dive opisał przekazanie przez pracowników Samsunga poufnego kodu i materiałów ze spotkania do ChatGPT. Relacja opiera się na doniesieniach koreańskiej prasy; Samsung nie odpowiedział na prośbę redakcji o komentarz. Jest to doniesienie o ujawnieniu przez użytkowników, a nie ustalenie, że OpenAI wykorzystało materiał ponownie lub udostępniło go innym klientom. [Relacja z 10 kwietnia 2023 r.](https://www.cybersecuritydive.com/news/Samsung-Electronics-ChatGPT-leak-data-privacy/647219/).

**Wniosek dla firmy:** Uprawnienie pracownika do odczytu pliku należy oceniać odrębnie od zgody na przekazanie go zewnętrznej usłudze AI. Zatwierdzenie powinno wskazywać dozwolone informacje, zadanie i ścieżkę dostępu.

### 3.2 Awaria dostawcy: ChatGPT, marzec 2023

OpenAI poinformowało, że błąd umożliwił niektórym użytkownikom zobaczenie cudzych tytułów rozmów i potencjalnie pierwszej wiadomości. Możliwa ekspozycja danych płatniczych dotyczyła 1,2% abonentów Plus aktywnych w określonym dziewięciogodzinnym oknie. Pełne numery kart nie zostały ujawnione. Był to opisany przez dostawcę błąd izolacji, a nie dowód treningu na ujawnionych danych. [Raport OpenAI z 24 marca 2023 r.](https://openai.com/index/march-20-chatgpt-outage/).

**Wniosek dla firmy:** Prawidłowe działanie pracownika nie eliminuje ryzyka po stronie dostawcy. Ocena dostawcy powinna obejmować powiadamianie o incydentach, wsparcie wyjaśnienia zdarzenia i wrażliwość powierzanych informacji.

### 3.3 Nieopublikowane badania: co wynika ze sporu matematyków

Poprzedni rozdział wprowadza ten spór. Relacje uczestników pozwalają na następujące, ograniczone podsumowanie dowodów:

| Dowód | Co potwierdza | Czego nie potwierdza |
| --- | --- | --- |
| Oświadczenie Buckmastera | Opis osobistej współpracy z Alpögem, przekazywania szkiców do Codex i niepewności co do ich użycia | Działania instytucjonalnego Anthropic lub udowodnionego przywłaszczenia |
| Aktualizacja OpenAI z 10 września 2026 r. | Deklarację wykluczenia wpływu promptów Buckmastera z poprzednich dwóch miesięcy, także przez trening | Niezależnego audytu lub ustaleń dotyczących danych wszystkich użytkowników |

Źródła: [oświadczenie Buckmastera](https://cims.nyu.edu/~tristanb/statement.pdf), [stanowisko i aktualizacja OpenAI](https://openai.com/index/navier-stokes-solution/).

**Wniosek dla firmy:** Podobieństwo i kolejność zdarzeń mogą rodzić pytania, ale nie dowodzą związku przyczynowego. Firma potrzebuje datowanych zapisów pracy oraz informacji, co przekazała, z jakiego konta, przy jakich ustawieniach i warunkach umownych. Dane osobowe to tylko jeden z obszarów: nieopublikowana metoda może zachować wartość handlową po usunięciu nazwisk.

### 3.4 Postępowania prawne: zarzuty a obowiązujące rozstrzygnięcie

Włoski Garante ogłosił w 2024 r. karę 15 mln euro dotyczącą ChatGPT. Zaktualizowany komunikat odnotowuje skuteczne zaskarżenie w marcu 2026 r. [Komunikat regulatora z aktualizacją](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432).

18 marca 2026 r. sąd w Rzymie uchylił decyzję z przyczyn dotyczących właściwości regulatora w ramach współpracy organów na gruncie RODO. Pozostałych podstaw zaskarżenia nie rozstrzygnięto. Kary nie należy przedstawiać jako nadal obowiązującej, a uchylenia jako merytorycznego oczyszczenia ze wszystkich zarzutów. To postępowanie jest odrębne od sporu matematyków. [Wyrok, zwłaszcza końcowe uzasadnienie i sentencja](https://dei.web.uniroma1.it/sites/default/files/allegati/2026-05/Trib_Roma_OpenAI_Garante_2026.pdf).

**Wniosek dla firmy:** Rejestr spraw powinien wskazywać etap postępowania, datę decyzji, wynik i jego zakres. Zarzut, decyzja regulatora i wyrok sądu mają różną wartość dowodową.

### 3.5 Wymagania do dalszej analizy nadzoru

Poniższe punkty są proponowanymi wymaganiami firmowymi wynikającymi z przypadków, a nie ustaleniami dotyczącymi istniejących funkcji produktów:

| Obawa biznesowa | Proponowane wymaganie | Dowód do zatwierdzenia |
| --- | --- | --- |
| Niezatwierdzone przekazanie | Zgoda właściciela informacji i minimalny niezbędny zakres danych | Klasyfikacja, dozwolone zadanie i zatwierdzona ścieżka |
| Awaria dostawcy | Określone obowiązki przy incydencie i akceptowalny zakres ekspozycji | Warunki powiadamiania, kontakty i procedura reagowania |
| Możliwe wtórne wykorzystanie | Ocena dozwolonych celów przetwarzania wykraczająca poza trening | Właściwa umowa, ustawienia konta i nierozstrzygnięte pytania |
| Utrata pierwszeństwa badań | Zachowanie historii pochodzenia bez zbędnego kopiowania treści | Datowane szkice, identyfikatory wersji i chroniony rejestr przekazania |
| Brak możliwości wyjaśnienia zdarzenia | Określenie dostępu do dowodów i ich retencji przed użyciem | Identyfikatory żądań, rejestry dostępu i ścieżka eskalacji do dostawcy |

Nie należy kopiować poufnych promptów do ogólnodostępnych logów tylko dla poprawy rozliczalności. Gdy to wystarcza, należy zapisywać identyfikatory i metadane; niezbędne archiwum treści wymaga własnych zasad dostępu i retencji.

**Rezultat:** Rejestr ryzyk oparty na dowodach, stanowiący podstawę decyzji o nadzorze w rozdziale 4. Dla każdego zastosowania należy zapisać zagrożone informacje, scenariusz utraty kontroli, proponowane zabezpieczenie, dowody, pozostającą niepewność i osobę uprawnioną do jej zaakceptowania.
