## 4. Perspektywa polityk i umów OpenAI

Zobowiązania OpenAI trzeba oceniać w odniesieniu do usługi rzeczywiście kupowanej przez firmę i przyjętych warunków. Poniższe dokumenty odpowiadają na różne pytania: co strony mogą robić z informacjami, jak przetwarzane są dane osobowe, jakie zastosowania są dozwolone i jakie zabezpieczenia są dostępne. W praktyce poufność biznesowa łączy obowiązki umowne z konfiguracją; nie oznacza zapewnienia, że OpenAI technicznie nie może uzyskać dostępu do treści.

### 4.1 Ustalenie właściwych dokumentów

Dla usług indywidualnych w Polsce punktem wyjścia są Europe Terms of Use; usługi biznesowe podlegają osobnej ścieżce umownej. Płatnego konta osobistego nie należy traktować jak odpowiednika umowy firmowej. [Europe Terms of Use, postanowienia wstępne](https://openai.com/policies/eu-terms-of-use/).

| Dokument | Pytanie do rozstrzygnięcia |
| --- | --- |
| [Services Agreement](https://openai.com/policies/services-agreement/) oraz zamówienie lub indywidualna umowa firmy | Co OpenAI uzgodniło z tą firmą? |
| [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/) | Jakie zasady dotyczą danych osobowych przetwarzanych w imieniu firmy? |
| [Service Terms](https://openai.com/policies/service-terms/) | Co zmienia włączenie konkretnej funkcji? |
| [Usage Policies](https://openai.com/policies/usage-policies/revisions/2025-10-29/) | Czy planowane działanie jest dozwolone? |

Dla Codex należy zapisać sposób logowania i połączenia z dostawcą. Uwierzytelnianie wpływa na właściwe mechanizmy kontroli i zasady postępowania z danymi; dodanie LiteLLM do ścieżki samo w sobie nie zmienia umowy. [Uwierzytelnianie Codex](https://learn.chatgpt.com/docs/auth).

### 4.2 Poufność i dozwolone wykorzystanie treści biznesowych

Punkty 4.2 i 7 Services Agreement ograniczają wykorzystanie treści, wymagają wyraźnej zgody na ulepszanie usług i nakładają obowiązki poufności. Dopuszczają określone ujawnienia, w tym niezbędnym odbiorcom związanym poufnością i wymagane prawem. Są to zobowiązania umowne z wyjątkami, a nie bezwzględny zakaz dostępu. [Services Agreement, pkt 4.2 i 7](https://openai.com/policies/services-agreement/).

**Decyzja firmy:** Traktować nieopublikowane metody i badania jako poufne również po usunięciu identyfikatorów osobowych. Własność, poufność i dozwolone ponowne wykorzystanie rozpatrywać osobno. Przed dopuszczeniem kluczowego know-how ocenić środki ochrony prawnej i odpowiedzialność z przyjętej umowy, zamiast zakładać pełną rekompensatę każdej straty.

### 4.3 Trening modeli i wtórne wykorzystanie

OpenAI odróżnia treści usług indywidualnych, które mogą służyć do treningu z uwzględnieniem ustawień, od biznesowych danych wejściowych i wyników, niewykorzystywanych do treningu domyślnie. Opisuje też możliwość wyraźnego udostępnienia danych API, w tym przez feedback. Zgody treningowe wymagają więc sprawdzenia wraz z typem konta i ustawieniami administratora. [Polityka ulepszania modeli](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).

**Decyzja firmy:** Wyłączyć niezatwierdzone udostępnianie i przejrzeć sposób przekazywania feedbacku. Wyłączenie treningu nie zastępuje ograniczeń innych zastosowań, przechowywania ani dalszego przekazywania.

### 4.4 Dane osobowe i DPA

DPA reguluje dane osobowe przetwarzane w imieniu klienta. Obejmuje udokumentowane instrukcje, poufność, zgłaszanie naruszeń, warunkowe prawa audytowe, podwykonawców i zwrot lub usuwanie z wyjątkami prawnymi. Definicja Customer Data jest węższa niż cała wiedza biznesowa. [DPA, pkt 1–4 i 6](https://openai.com/policies/data-processing-addendum/).

Europe Privacy Policy wyraźnie wyłącza ze swojego zakresu treści przetwarzane w imieniu klientów biznesowych i odsyła do umów z klientami. Nie należy używać tej polityki jako jedynej podstawy zatwierdzenia przetwarzania treści firmowych. [Europe Privacy Policy, zakres](https://openai.com/policies/eu-privacy-policy/).

**Decyzja firmy:** Ustalić właściwe role dotyczące prywatności, cel przetwarzania, uprawnienie do ujawnienia, zasady transferów i instrukcje retencji. Know-how niebędące danymi osobowymi oceniać również w świetle zobowiązań poufności.

### 4.5 Bezpieczeństwo, dostęp i przechowywanie

Oświadczenie OpenAI dotyczące prywatności biznesowej opisuje szyfrowanie, ograniczenia dostępu i właściwe dla produktów okoliczności dostępu upoważnionego personelu. Opisy te nie oznaczają, że dostawca nie może przetwarzać informacji w czytelnej postaci. [Enterprise privacy](https://openai.com/enterprise-privacy/).

Kontrola retencji API ma warunki i wyjątki właściwe dla punktów końcowych. Brak treningu, brak retencji i brak dostępu ludzi to różne zapewnienia. [Kontrola danych API](https://developers.openai.com/api/docs/guides/your-data).

**Decyzja firmy:** Zatwierdzić konkretny profil retencji i dostępu dla każdej ścieżki. Uwzględnić lokalny stan Codex i kopie firmowej bramy; ustawienia OpenAI nie usuwają tych magazynów.

### 4.6 Podwykonawcy, integracje i warunki funkcji

OpenAI publikuje podwykonawców wraz z produktami, lokalizacjami i celami przetwarzania. Wykaz należy wykorzystać do oceny wybranej usługi, zamiast zakładać jednego odbiorcę lub jeden kraj przetwarzania. [Lista podwykonawców](https://openai.com/policies/sub-processor-list/).

Service Terms dodają postanowienia właściwe dla funkcji, w tym zastrzeżenia dla bety, administrowanie, udostępnianie GPT i zewnętrzne Apps. Włączenie funkcji może zmienić odbiorców i uprawnienia; ogólne zatwierdzenie przestrzeni roboczej nie wystarcza. [Service Terms, pkt 2, 3, 5 i 7](https://openai.com/policies/service-terms/).

**Decyzja firmy:** Osobno zatwierdzać hosting LiteLLM, skanery, systemy logowania i narzędzia zewnętrzne. Same zobowiązania OpenAI nie uzasadniają ich dostępu.

### 4.7 Dozwolone użycie i wersje polityk

Usage Policies nakładają obowiązki na użytkowników, w tym dotyczące prywatności, bezpieczeństwa i ograniczenia niektórych działań. Nie zastępują obowiązków dostawcy w zakresie poufności i nie czynią zgodnym z prawem ujawnienia, do którego brakuje uprawnienia. [Usage Policies](https://openai.com/policies/usage-policies/revisions/2025-10-29/).

Data oceny to **2 listopada 2026 r.** Właściwa jest wersja obowiązująca od **29 października 2025 r.** [Ogólna strona zasad](https://openai.com/en-GB/policies/usage-policies/) wyświetla obecnie wersję obowiązującą od **20 listopada 2026 r.**; należy oznaczyć ją jako nadchodzącą i wcześniej ocenić skutki zmiany.

### 4.8 Dokumentacja dopuszczenia do wdrożenia

Firma powinna zachować zapis zatwierdzenia łączący ocenę umowną z wdrożoną konfiguracją. Jest to materiał potrzebny do wyjaśnienia, dlaczego dany sposób pracy został dopuszczony.

- Wskazać podmiot prawny, przyjęte umowy, usługę, przestrzeń lub projekt API i wersje.
- Zapisać dozwolone kategorie danych, zgody na udostępnianie do treningu, retencję i odbiorców.
- Zapisać zatwierdzenia integracji, dowody konfiguracji i osoby odpowiedzialne.
- Ocenić środki ochrony poufności, odpowiedzialność, wyłączenia dla funkcji i procedury incydentów względem wartości informacji.
- Ponawiać ocenę po zmianach warunków, funkcji produktu, uwierzytelniania i przepływów danych.

W tym dokumencie **zobowiązanie umowne** oznacza warunek wiążący strony, **opis dostawcy** przedstawia zamierzone działanie, a **dowód z wdrożenia** pokazuje zaobserwowane zabezpieczenia. Wszystkie trzy wspierają zatwierdzenie; żaden pojedynczo nie potwierdza ochrony przed każdym ryzykiem poufności. Rozdziały o przepływach danych i technice określają wymagania konfiguracji i testów.

