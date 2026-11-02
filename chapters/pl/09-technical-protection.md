## 9. Zabezpieczenia techniczne i ich ograniczenia

Mechanizmy bezpieczeństwa chronią przed konkretnymi zagrożeniami. Szyfrowanie może zabezpieczać połączenie lub zapisane dane, kontrola dostępu ograniczać grono uprawnionych użytkowników, a środowisko izolowane agenta, czyli sandbox, ograniczać działania na komputerze. Mechanizmy te nie zapewniają jednak takiej samej ochrony przed operatorem usługi ani przed ujawnieniem dokonanym przez osobę uprawnioną, ale niezgodnie z zasadami.

**Szkic rozdziału**

- Wyjaśnienie szyfrowania podczas transmisji i przechowywania oraz kluczy zarządzanych przez klienta, z określeniem elementów systemu, które nadal mogą odszyfrować dane.
- Ocena izolacji kont, dostępu opartego na rolach, dostępu administracyjnego i rejestrowania dostępu w wybranych produktach.
- Rozróżnienie ograniczeń sieciowych i sandboxingu agenta od ograniczeń dotyczących tego, co OpenAI może zrobić z otrzymaną treścią.
- Wyjaśnienie confidential computing i atestacji jako silniejszych opcji architektonicznych wyłącznie tam, gdzie ich użycie jest udokumentowane i ma zastosowanie; bez zakładania ich obecności w standardowym ChatGPT lub Codex.
- Ocena raportów audytowych na podstawie zakresu systemów, okresu badania, sprawdzonych zabezpieczeń i wyjątków, a nie samych oznaczeń certyfikacyjnych.

Przewodnik bezpieczeństwa Codex opisuje łączenie mechanizmów firmowych z istniejącą ochroną tożsamości, urządzeń i sieci. Stanowi podstawę przeglądu konfiguracji, a nie dowód, że wdrożenie w tej firmie jest już bezpieczne. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).

**Planowany rezultat:** Macierz zabezpieczeń wskazująca zagrożenie, mechanizm, dowody, ograniczenia i zakres zaufania nadal wymaganego wobec dostawcy.

