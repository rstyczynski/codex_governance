## Źródła i referencje

Poniższe źródła publiczne sprawdzono **2 listopada 2026 r.** Daty obowiązywania należy zapisywać oddzielnie od dat dostępu. Aktualizowaną dokumentację i odnośniki trzeba ponownie sprawdzić przed wdrożeniem. Dokumentacja producenta potwierdza opisywane funkcje; gwarancje dla konkretnego wdrożenia wymagają właściwej umowy, konfiguracji i dowodów weryfikacji.

### Umowy i dokumentacja techniczna OpenAI

1. **OpenAI. [Services Agreement](https://openai.com/policies/services-agreement/).** Strona oznaczona jako zaktualizowana 1 grudnia 2025 r., z datą obowiązywania 1 stycznia 2026 r. Podstawa przeglądu zakresu usług biznesowych, Customer Content, poufności i dozwolonego przetwarzania. Powiązane rozdziały: 5, 6, 8, 9, 10.
2. **OpenAI. [Usage Policies — wersja obowiązująca od 29 października 2025 r.](https://openai.com/policies/usage-policies/revisions/2025-10-29/).** Referencja zasad dozwolonego użycia właściwa dla daty oceny w tym szkicu; nie zastępuje zobowiązań dostawcy do poufności. Powiązane rozdziały: 5, 6.
3. **OpenAI. [Usage Policies — ogólna strona](https://openai.com/en-GB/policies/usage-policies/).** Referencja przekazana przez użytkownika. W chwili sprawdzania wyświetla wersję obowiązującą od 20 listopada 2026 r.; należy śledzić ją osobno jako nadchodzącą. Powiązany rozdział: 5.
4. **OpenAI. [Data controls in the OpenAI platform](https://developers.openai.com/api/docs/guides/your-data).** Wykorzystanie i przechowywanie danych API, ZDR, ograniczenia punktów końcowych i lokalizacja danych. Powiązane rozdziały: 8, 10.
5. **OpenAI. [Codex authentication](https://learn.chatgpt.com/docs/auth).** Sposoby uwierzytelniania i ich związek z mechanizmami administracyjnymi oraz zasadami postępowania z danymi. Powiązane rozdziały: 7, 8, 11.
6. **OpenAI. [Connect to a gateway](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).** Konfiguracja bramy, uwierzytelnianie po stronie dostawcy i granice między żądaniami do modelu a pozostałym ruchem. Powiązane rozdziały: 7, 11, 12.
7. **OpenAI. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).** Konfiguracja firmowa, weryfikacja oraz łączenie mechanizmów kontroli dostępu i działań. Powiązane rozdziały: 6, 9, 13, 14.

### Brama, DLP i zabezpieczenia sieciowe

8. **LiteLLM. [Connect Codex CLI to LiteLLM](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli).** Referencja integracji; wymaga sprawdzenia dla wybranych wersji i sposobu uwierzytelniania. Powiązany rozdział: 11.
9. **LiteLLM. [Guardrails — Quick Start](https://docs.litellm.ai/docs/proxy/guardrails/quick_start).** Integracje kontroli treści i moment egzekwowania reguł. Powiązane rozdziały: 11, 13.
10. **LiteLLM. [Logging](https://docs.litellm.ai/docs/proxy/logging).** Miejsca docelowe logów i mechanizmy kontroli; należy ocenić możliwość powstawania dodatkowych kopii treści. Powiązane rozdziały: 10, 11, 14.
11. **Oracle. [Overview of the Network Firewall Service](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm).** Możliwości OCI Network Firewall i zakres ruchu kierowanego przez usługę. Powiązany rozdział: 12.
12. **Palo Alto Networks. [What Is Supported with AI Access Security](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).** Obsługa aplikacji przez DLP i wymagania; nie stanowi dowodu włączenia tych funkcji do OCI Network Firewall. Powiązane rozdziały: 12, 13.
13. **Cloudflare. [Set up HTTP filtering](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).** Przykład implementacji kierowania ruchu, certyfikatów i inspekcji WWW; uwzględnienie źródła nie oznacza wyboru produktu. Powiązany rozdział: 12.

### Spór badawczy i przekazane materiały kontekstowe

14. **Tristan Buckmaster. [Publiczne oświadczenie dotyczące pracy z Leventem Alpögem i kontaktów z OpenAI](https://cims.nyu.edu/~tristanb/statement.pdf).** Pierwotna relacja badacza; opisuje prywatny charakter współpracy i niepewność dotyczącą wykorzystania danych. Powiązane rozdziały: 2, 3.
15. **OpenAI. [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution/).** Publikacja z 8 września 2026 r., z aktualizacją dotyczącą dochodzenia z 10 września 2026 r. Relacja dostawcy i odpowiedź na zgłoszone obawy. Powiązane rozdziały: 2, 3.
16. **Andrew Orlowski / Onet, źródło przypisane The Telegraph. [Artykuł o zarzutach matematyków dotyczących ich odkryć](https://wiadomosci.onet.pl/swiat/najwiekszy-skandal-w-historii-nauki-znani-matematycy-twierdza-ze-ai-ukradla-ich/4s4mvnq).** Publikacja z 16 września 2026 r. Przekazany przez użytkownika materiał wtórny służący jako kontekst, a nie niezależny dowód niewłaściwego wykorzystania danych. Powiązany rozdział: 2.
17. **Krzysztof Sulikowski / GeekWeek Interia. [Artykuł o ogłoszeniach matematycznych OpenAI i Anthropic](https://geekweek.interia.pl/technologia/sztuczna-inteligencja/news-wstrzas-w-nauce-openai-i-anthropic-przedstawily-dowody-tego,nId,23565804).** Przekazany przez użytkownika materiał wtórny dotyczący odrębnych ogłoszeń; należy zachować rozróżnienie od sporu o prywatne sesje. Powiązany rozdział: 2.
18. **Fragment przekazany przez użytkownika. Generative Chat at Oracle: Terms of Use & Disclaimer.** Nie przekazano publicznego URL, wersji ani daty obowiązywania. Wykorzystany wyłącznie jako przykład projektowania polityki. Stwierdzenia o zatwierdzeniu przez CSSAP i Oracle Legal, kluczach zarządzanych przez Oracle i dozwolonych kategoriach danych nie zostały niezależnie zweryfikowane i nie potwierdzają równoważnej ochrony w innym wdrożeniu. Powiązany rozdział: 6.

### Konfiguracja lokalna i cykl życia danych

19. **OpenAI. [Podstawy konfiguracji](https://learn.chatgpt.com/docs/config-file/config-basic).** Poziomy konfiguracji, kolejność pierwszeństwa i rozróżnienie ustawień domyślnych od wymuszanych wymagań. Powiązane rozdziały: 7, 14.
20. **OpenAI. [Konfiguracja zaawansowana](https://learn.chatgpt.com/docs/config-file/config-advanced).** Konfiguracja użytkownika, nadpisania projektu i przykłady przechowywania stanu lokalnego oraz poświadczeń. Powiązane rozdziały: 7, 10.
21. **OpenAI. [Zmienne środowiskowe](https://learn.chatgpt.com/docs/config-file/environment-variables).** `CODEX_HOME` i konfigurowalne lokalizacje stanu SQLite. Powiązany rozdział: 7.
22. **OpenAI. [Referencja konfiguracji](https://learn.chatgpt.com/docs/config-file/config-reference).** Obsługiwane klucze i ograniczenia zakresu; ustawień historii nie należy traktować jako globalnej kontroli usuwania. Powiązane rozdziały: 7, 10, 14.
23. **OpenAI. [Instrukcje własne z AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).** Wyszukiwanie instrukcji użytkownika i projektu oraz włączanie ich do kontekstu. Powiązane rozdziały: 7, 13.
24. **OpenAI. [Pamięci](https://learn.chatgpt.com/docs/customization/memories).** Zapis, ponowne wykorzystanie i kontrola pamięci lokalnej Codex, odrębnej od pamięci ChatGPT w przeglądarce. Powiązane rozdziały: 7, 10.
25. **OpenAI. [Diagnostyka](https://learn.chatgpt.com/docs/reference/troubleshooting).** Lokalizacje sesji, archiwów sesji i logów aplikacji; przegląd danych poufnych przed przekazaniem diagnostyki. Powiązane rozdziały: 7, 10, 14.
26. **OpenAI. [Projekty i rozmowy](https://learn.chatgpt.com/docs/projects).** Wspólny kontekst projektu ChatGPT, odrębny od lokalnego repozytorium i stanu Codex. Powiązany rozdział: 7.

### Dodatkowe źródła polityk i umów OpenAI

27. **OpenAI. [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/).** Aktualizacja 1 grudnia 2025 r.; obowiązuje od 1 stycznia 2026 r. Warunki przetwarzania danych osobowych, instrukcje, zgłaszanie naruszeń, warunki audytu i usuwanie. Powiązany rozdział: 5.
28. **OpenAI. [Europe Terms of Use](https://openai.com/policies/eu-terms-of-use/).** Aktualizacja 16 stycznia 2026 r. Warunki usług indywidualnych dla EOG, Szwajcarii i Wielkiej Brytanii; odrębne od umów biznesowych. Powiązany rozdział: 5.
29. **OpenAI. [Europe Privacy Policy](https://openai.com/policies/eu-privacy-policy/).** Aktualizacja 24 sierpnia 2026 r. Informacja o prywatności danych osobowych; wyłącza treści biznesowe przetwarzane w imieniu klienta. Powiązany rozdział: 5.
30. **OpenAI. [Service Terms](https://openai.com/policies/service-terms/).** Aktualizacja 16 października 2026 r. Dodatkowe postanowienia właściwe dla funkcji. Powiązany rozdział: 5.
31. **OpenAI. [Enterprise privacy](https://openai.com/enterprise-privacy/).** Aktualizacja 8 stycznia 2026 r. Opis dostawcy dotyczący ochrony danych biznesowych i dostępu. Powiązany rozdział: 5.
32. **OpenAI. [Lista podwykonawców](https://openai.com/policies/sub-processor-list/).** Aktualizacja 14 października 2026 r. Odbiorcy, zakres usług, cele i lokalizacje przetwarzania. Powiązany rozdział: 5.
33. **OpenAI. [How your data is used to improve model performance](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).** Aktualizacja 13 marca 2026 r. Rozróżnienie treningu dla usług indywidualnych i biznesowych oraz zgody na udostępnianie danych. Powiązany rozdział: 5.

### Dodatkowe źródła incydentów i postępowań prawnych

34. **Cybersecurity Dive. [Samsung employees leaked corporate data in ChatGPT: report](https://www.cybersecuritydive.com/news/Samsung-Electronics-ChatGPT-leak-data-privacy/647219/).** Publikacja z 10 kwietnia 2023 r.; ponownie sprawdzona 2 listopada 2026 r. Wtórna relacja o przekazywaniu danych przez pracowników, nie dowód wtórnego użycia przez dostawcę. Powiązany rozdział: 3.
35. **OpenAI. [March 20 ChatGPT outage: Here’s what happened](https://openai.com/index/march-20-chatgpt-outage/).** Publikacja z 24 marca 2023 r.; ponownie sprawdzona 2 listopada 2026 r. Raport dostawcy o incydencie. Powiązany rozdział: 3.
36. **Garante. [Komunikat o postępowaniu dotyczącym ChatGPT, z aktualizacją o wyniku sądowym](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432).** Ponownie sprawdzony 2 listopada 2026 r.; pierwotną informację o karze należy czytać łącznie z aktualizacją. Powiązany rozdział: 3.
37. **Tribunale di Roma. [Wyrok w sprawie zaskarżenia przez OpenAI decyzji Garante 755/2024](https://dei.web.uniroma1.it/sites/default/files/allegati/2026-05/Trib_Roma_OpenAI_Garante_2026.pdf).** Orzeczenie z 18 marca 2026 r.; kopia udostępniona przez Uniwersytet Sapienza, ponownie sprawdzona 2 listopada 2026 r. Podstawy i sentencja na stronach 5–7. Powiązany rozdział: 3.
