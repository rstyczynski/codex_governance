# Poufność danych i ochrona know-how przy korzystaniu z ChatGPT i Codex

**Wersja:** 0.3 — rozwinięty rozdział o politykach i umowach; pozostałe rozdziały w szkicu  
**Data:** 2 listopada 2026 r.  
**Odbiorcy:** Przedsiębiorcy, osoby zarządzające technologią, zespoły bezpieczeństwa i doradcy prawni  
**Status:** Wersja robocza; proponowane zabezpieczenia i polityka wymagają zatwierdzenia w organizacji oraz weryfikacji technicznej.

## Wprowadzenie

ChatGPT i Codex mogą pomagać firmie w analizowaniu dokumentów, tworzeniu oprogramowania i rozwijaniu nowych pomysłów. Takie działania mogą jednak również ujawniać zewnętrznym systemom informacje o klientach, kod źródłowy, strategie handlowe oraz nieopublikowane wyniki badań. Z perspektywy przedsiębiorcy najważniejsze jest uzyskanie użytecznego wsparcia przy zachowaniu kontroli nad tym, kto otrzymuje informacje, jak je wykorzystuje i jak długo pozostają dostępne.

Dokument koncentruje się na OpenAI: ChatGPT, Codex i OpenAI API. LiteLLM, firewalle sieciowe, serwery proxy HTTP oraz systemy zapobiegania wyciekom danych (Data Loss Prevention, DLP) są rozpatrywane jako zabezpieczenia dostępu do OpenAI, a nie jako alternatywni dostawcy modeli. Oracle Cloud Infrastructure (OCI) jest rozważane jako możliwe środowisko uruchomienia infrastruktury i egzekwowania reguł sieciowych.

Proponowane podejście łączy politykę firmową, techniczne egzekwowanie zasad i weryfikację działania. Polityka określa dozwolone informacje i zastosowania. Zabezpieczenia techniczne ograniczają dostęp i kontrolują obsługiwane przepływy danych. Weryfikacja pozwala ustalić, czy zabezpieczenia działają w rzeczywistym wdrożeniu. Żaden z tych elementów nie zastępuje oceny zobowiązań umownych OpenAI oraz zakresu zaufania, które nadal trzeba pokładać w dostawcy.

Każdy rozdział rozpoczyna się akapitem wprowadzającym. Rozdział 4 rozwinięto na podstawie oficjalnych dokumentów OpenAI; pozostałe rozdziały zachowują szkice do dalszego opracowania. Stwierdzenia oparte na źródłach zawierają odnośniki do dokumentów. Proponowane wymagania firmowe są założeniami projektowymi, a nie zapewnieniami, że dany produkt już je realizuje. Rozważana architektura podstawowa kieruje zatwierdzone żądania do modeli przez kontrolowaną przez firmę bramę LiteLLM i blokuje niezatwierdzony dostęp bezpośredni. Nie została jeszcze wdrożona ani przetestowana.

## Spis treści

### Część I — Wyzwania biznesowe

- [Rozdział 1 — Poufność i zasoby informacyjne firmy](chapters/pl/01-confidentiality-and-business-assets.md)

### Część II — Przypadek biznesowy: poufne badania

- [Rozdział 2 — Poufne badania i spór dotyczący matematyki](chapters/pl/02-confidential-research.md)

### Część III — Nadzór: odpowiedź na wyzwania biznesowe

- [Rozdział 3 — Nadzór: od ryzyka biznesowego do kryteriów zatwierdzenia](chapters/pl/03-governance.md)

### Część IV — Zasoby firmy, umowy i polityka firmowa

- [Rozdział 4 — Perspektywa polityk i umów OpenAI](chapters/pl/04-openai-policy-and-contracts.md)
- [Rozdział 5 — Projekt zasad firmowych](chapters/pl/05-company-rules.md)

### Część V — Kontekst techniczny i ograniczenia ochrony

- [Rozdział 6 — Przepływy danych w ChatGPT i Codex](chapters/pl/06-data-flows.md)
- [Rozdział 7 — Konta, uwierzytelnianie i zakres usług](chapters/pl/07-accounts-and-authentication.md)
- [Rozdział 8 — Zabezpieczenia techniczne i ich ograniczenia](chapters/pl/08-technical-protection.md)
- [Rozdział 9 — Przechowywanie, usuwanie i Zero Data Retention](chapters/pl/09-retention-deletion-and-zdr.md)

### Część VI — Proponowana architektura i egzekwowanie zasad

- [Rozdział 10 — Proponowana architektura z LiteLLM](chapters/pl/10-litellm-architecture.md)
- [Rozdział 11 — Egzekwowanie reguł sieciowych i OCI Network Firewall](chapters/pl/11-network-enforcement-and-oci.md)
  - Planowany zakres: DNS, proxy HTTP i firewalle dla dostępu przez przeglądarkę, CLI i API, w tym ograniczenia dostępu bezpośredniego i testy obchodzenia zabezpieczeń.
- [Rozdział 12 — DLP i ograniczenia działań agentów](chapters/pl/12-dlp-and-agent-controls.md)

### Część VII — Weryfikacja, utrzymanie i reagowanie na incydenty

- [Rozdział 13 — Weryfikacja, utrzymanie i reagowanie na incydenty](chapters/pl/13-validation-and-incident-response.md)

### Źródła i referencje

- [Źródła i referencje](chapters/pl/14-references.md)
