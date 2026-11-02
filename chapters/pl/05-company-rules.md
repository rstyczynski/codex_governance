## 5. Projekt zasad firmowych

Zasady firmowe przekładają ocenę ryzyka na instrukcje, których pracownicy mogą przestrzegać. Poniższy projekt stanowi propozycję podstawowych zasad do zatwierdzenia i wykorzystuje przekazany przykład Oracle jako wzorzec organizacyjny. Nie przenosi na tę firmę zatwierdzeń Oracle, zapewnień o zarządzaniu kluczami ani ustaleń umownych.

### Proponowane zasady dla pracowników

1. **Zatwierdzone środowisko.** Informacje firmowe niebędące publicznymi wolno przetwarzać wyłącznie przez usługi i ścieżki dostępu wymienione w rejestrze zatwierdzonych usług. Konta osobiste nie są dopuszczone do tego celu.
2. **Minimalny niezbędny zakres.** Należy przekazywać wyłącznie informacje potrzebne do zadania. Dostęp do dokumentu nie oznacza automatycznie uprawnienia do ujawnienia go usłudze AI.
3. **Treści wyłączone.** Standardowe środowisko nie może otrzymywać haseł, kluczy prywatnych, tokenów dostępu, kodów uwierzytelniających, pełnych numerów kart płatniczych ani kodów weryfikacyjnych kart. Sekrety uwierzytelniające należy przekazywać przez zatwierdzone mechanizmy uwierzytelniania, bez włączania ich do kontekstu modelu.
4. **Informacje wrażliwe i objęte regulacjami.** Informacje zdrowotne, inne szczególnie wrażliwe dane osobowe, informacje niejawne i dane objęte ograniczeniami kontraktów publicznych lub obronnych wymagają osobno zatwierdzonego środowiska. Należy uwzględnić kategorie PHI, FCI i CUI, jeśli mają zastosowanie do obowiązków firmy.
5. **Informacje klientów i partnerów.** Nie wolno przekazywać informacji, których przetwarzanie naruszałoby NDA, umowę, obowiązek prawny lub zatwierdzony cel ich zebrania.
6. **Know-how.** Nieopublikowane wynalazki, badania, plany strategiczne, własne metody i kluczowy kod źródłowy wymagają zgody właściciela informacji oraz osoby odpowiedzialnej za bezpieczeństwo przed przetwarzaniem zewnętrznym.
7. **Prace prawne i inne czynności zawodowe.** AI może wspierać zatwierdzone prace przygotowawcze i analizy. Wnioski i porady zawodowe wymagają właściwej weryfikacji przez osobę o odpowiednich kwalifikacjach; wynik AI nie stanowi zatwierdzenia przez firmę.
8. **Uprawnienia Codex.** Należy udostępniać wyłącznie niezbędne repozytoria, katalogi, narzędzia i połączenia sieciowe. Zmiany produkcyjne, transfery zewnętrzne i publikacja podlegają firmowej procedurze zatwierdzania.
9. **Integracje i udostępnianie.** Nowe wtyczki, serwery MCP, konektory, linki udostępniające i skanery zewnętrzne wymagają zatwierdzenia. Pracownicy nie mogą zmieniać ustawień udostępniania danych do treningu ani ustawień bezpieczeństwa poza zakresem swoich uprawnień.
10. **Zgłaszanie incydentów.** Przypadkowe ujawnienie należy niezwłocznie zgłosić do **[kontakt do zgłaszania incydentów]**. Trzeba zachować identyfikatory i istotne dowody bez zbędnego kopiowania poufnych treści. Ujawnione dane uwierzytelniające należy niezwłocznie unieważnić.
11. **Wyjątki.** Należy zapisać cel, informacje, środowisko, zabezpieczenia, osoby zatwierdzające i datę wygaśnięcia. Wyjątek wewnętrzny nie uchyla prawa, umowy ani ograniczeń dostawcy.

### Odpowiedzialność i dokumentacja zatwierdzenia

| Odpowiedzialność | Proponowana osoba lub funkcja |
| --- | --- |
| Zatwierdzanie zastosowań biznesowych i akceptacja ryzyka pozostającego po wdrożeniu zabezpieczeń | Właściciel firmy lub osoba odpowiedzialna za dany obszar biznesowy |
| Klasyfikacja i zatwierdzanie wykorzystania informacji | Właściciel informacji |
| Konfiguracja i weryfikacja zabezpieczeń technicznych | Osoby odpowiedzialne za bezpieczeństwo i platformę |
| Przegląd umów i właściwych obowiązków | Doradca prawny; osoba odpowiedzialna za prywatność, jeśli dotyczy |
| Zgłaszanie błędów i przestrzeganie zatwierdzonych sposobów pracy | Każdy użytkownik |

**Planowany rezultat:** Krótka zatwierdzona polityka, karta środowiska i formularz wyjątku. Przed wydaniem należy uzupełnić **[nazwa firmy]**, **[zatwierdzone środowiska]**, **[osoby odpowiedzialne]** i **[kontakt do zgłaszania incydentów]**.

