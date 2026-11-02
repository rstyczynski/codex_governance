## 13. Weryfikacja, utrzymanie i reagowanie na incydenty

Zatwierdzenie powinno wynikać z wykazanej kontroli nad planowanymi sposobami pracy, a nie z samej instalacji produktów. Weryfikacja musi potwierdzić, że zatwierdzone zadania nadal dają się wykonywać, zabronione transfery są blokowane na objętych ochroną ścieżkach, a awarie nie wyłączają po cichu zabezpieczeń. Utrzymanie powinno zachowywać te właściwości mimo zmian produktów i zasad.

**Szkic rozdziału**

| Obszar weryfikacji | Dowód wymagany do odbioru pilotażu |
| --- | --- |
| Zatwierdzona ścieżka | Wywołania testowe aplikacji i Codex docierają przez LiteLLM do właściwej usługi OpenAI |
| Zapobieganie obejściu | Niezatwierdzony dostęp bezpośredni nie działa na zarządzanych urządzeniach, także podczas pracy zdalnej |
| Ochrona danych wejściowych | Syntetyczna treść objęta ograniczeniami jest blokowana przed przekazaniem do dostawcy |
| Awaria skanera | Obowiązkowe kontrole blokują żądanie przy awarii, bez automatycznego przejścia na połączenie bezpośrednie |
| Zakres funkcji | Każdy dopuszczony typ żądania ma udokumentowany test; nieobsługiwane ścieżki pozostają zablokowane |
| Poufność logów | Rutynowe logi, ślady diagnostyczne i eksporty nie zawierają sekretów dostępu ani testowych treści objętych ograniczeniami |
| Granice działań agenta | Próby odczytu zastrzeżonych ścieżek i niezatwierdzonych transferów zewnętrznych kończą się odmową |
| Granice konfiguracji | Efektywne ustawienia i zarządzane wymagania są sprawdzane przy nadpisaniach użytkownika, projektu i sesji |
| Cykl życia danych lokalnych | Syntetyczne znaczniki są śledzone w sesjach, włączonych pamięciach, plikach i kopiach zapasowych; usuwanie jest sprawdzane osobno dla każdego magazynu |
| Obsługa incydentu | Symulowane ujawnienie skutkuje zgłoszeniem, działaniami dotyczącymi danych uwierzytelniających i zapisem dowodów |

- Przypisanie odpowiedzialności za aktualizacje, bezpieczeństwo zależności, certyfikaty, zmiany reguł i przeglądy dostępu.
- Ustalenie zdarzeń wymagających przeglądu: nowe modele, zmiany warunków, nowe wersje aplikacji i dodatkowe integracje.
- Określenie ograniczania skutków incydentu, wymiany danych uwierzytelniających, kontaktu z dostawcą i oceny obowiązków zgłoszeniowych wynikających z umów lub prawa.
- Zapisanie ryzyka pozostającego po wdrożeniu zabezpieczeń, w szczególności niewykrytego know-how, dostępu uprawnionych odbiorców oraz niezarządzanych urządzeń osobistych poza kontrolowanym środowiskiem.
- Określenie warunków zatwierdzenia i planu wycofania wdrożenia przed wprowadzeniem poufnych danych produkcyjnych.

**Planowany rezultat:** Raport z pilotażu, instrukcja utrzymania, procedura incydentów i podpisana decyzja o wdrożeniu.

