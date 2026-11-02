## Źródła i referencje

Poniższe źródła publiczne sprawdzono **2 listopada 2026 r.** Daty obowiązywania należy zapisywać oddzielnie od dat dostępu. Aktualizowaną dokumentację i odnośniki trzeba ponownie sprawdzić przed wdrożeniem. Dokumentacja producenta potwierdza opisywane funkcje; gwarancje dla konkretnego wdrożenia wymagają właściwej umowy, konfiguracji i dowodów weryfikacji.

### Umowy i dokumentacja techniczna OpenAI

1. **OpenAI. [Services Agreement](https://openai.com/policies/services-agreement/).** Strona oznaczona jako zaktualizowana 1 grudnia 2025 r., z datą obowiązywania 1 stycznia 2026 r. Podstawa przeglądu zakresu usług biznesowych, Customer Content, poufności i dozwolonego przetwarzania. Powiązane rozdziały: 4, 5, 7, 8, 9.
2. **OpenAI. [Usage Policies — wersja obowiązująca od 29 października 2025 r.](https://openai.com/policies/usage-policies/revisions/2025-10-29/).** Referencja zasad dozwolonego użycia właściwa dla daty oceny w tym szkicu; nie zastępuje zobowiązań dostawcy do poufności. Powiązane rozdziały: 4, 5.
3. **OpenAI. [Usage Policies — ogólna strona](https://openai.com/en-GB/policies/usage-policies/).** Referencja przekazana przez użytkownika. W chwili sprawdzania wyświetla wersję obowiązującą od 20 listopada 2026 r.; należy śledzić ją osobno jako nadchodzącą. Powiązany rozdział: 4.
4. **OpenAI. [Data controls in the OpenAI platform](https://developers.openai.com/api/docs/guides/your-data).** Wykorzystanie i przechowywanie danych API, ZDR, ograniczenia punktów końcowych i lokalizacja danych. Powiązane rozdziały: 7, 9.
5. **OpenAI. [Codex authentication](https://learn.chatgpt.com/docs/auth).** Sposoby uwierzytelniania i ich związek z mechanizmami administracyjnymi oraz zasadami postępowania z danymi. Powiązane rozdziały: 6, 7, 10.
6. **OpenAI. [Connect to a gateway](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).** Konfiguracja bramy, uwierzytelnianie po stronie dostawcy i granice między żądaniami do modelu a pozostałym ruchem. Powiązane rozdziały: 6, 10, 11.
7. **OpenAI. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).** Konfiguracja firmowa, weryfikacja oraz łączenie mechanizmów kontroli dostępu i działań. Powiązane rozdziały: 5, 8, 12, 13.

### Brama, DLP i zabezpieczenia sieciowe

8. **LiteLLM. [Connect Codex CLI to LiteLLM](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli).** Referencja integracji; wymaga sprawdzenia dla wybranych wersji i sposobu uwierzytelniania. Powiązany rozdział: 10.
9. **LiteLLM. [Guardrails — Quick Start](https://docs.litellm.ai/docs/proxy/guardrails/quick_start).** Integracje kontroli treści i moment egzekwowania reguł. Powiązane rozdziały: 10, 12.
10. **LiteLLM. [Logging](https://docs.litellm.ai/docs/proxy/logging).** Miejsca docelowe logów i mechanizmy kontroli; należy ocenić możliwość powstawania dodatkowych kopii treści. Powiązane rozdziały: 9, 10, 13.
11. **Oracle. [Overview of the Network Firewall Service](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm).** Możliwości OCI Network Firewall i zakres ruchu kierowanego przez usługę. Powiązany rozdział: 11.
12. **Palo Alto Networks. [What Is Supported with AI Access Security](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).** Obsługa aplikacji przez DLP i wymagania; nie stanowi dowodu włączenia tych funkcji do OCI Network Firewall. Powiązane rozdziały: 11, 12.
13. **Cloudflare. [Set up HTTP filtering](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).** Przykład implementacji kierowania ruchu, certyfikatów i inspekcji WWW; uwzględnienie źródła nie oznacza wyboru produktu. Powiązany rozdział: 11.

### Spór badawczy i przekazane materiały kontekstowe

14. **Tristan Buckmaster. [Publiczne oświadczenie dotyczące pracy z Leventem Alpögem i kontaktów z OpenAI](https://cims.nyu.edu/~tristanb/statement.pdf).** Pierwotna relacja badacza; opisuje prywatny charakter współpracy i niepewność dotyczącą wykorzystania danych. Powiązany rozdział: 2.
15. **OpenAI. [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution/).** Publikacja z 8 września 2026 r., z aktualizacją dotyczącą dochodzenia z 10 września 2026 r. Relacja dostawcy i odpowiedź na zgłoszone obawy. Powiązany rozdział: 2.
16. **Andrew Orlowski / Onet, źródło przypisane The Telegraph. [Artykuł o zarzutach matematyków dotyczących ich odkryć](https://wiadomosci.onet.pl/swiat/najwiekszy-skandal-w-historii-nauki-znani-matematycy-twierdza-ze-ai-ukradla-ich/4s4mvnq).** Publikacja z 16 września 2026 r. Przekazany przez użytkownika materiał wtórny służący jako kontekst, a nie niezależny dowód niewłaściwego wykorzystania danych. Powiązany rozdział: 2.
17. **Krzysztof Sulikowski / GeekWeek Interia. [Artykuł o ogłoszeniach matematycznych OpenAI i Anthropic](https://geekweek.interia.pl/technologia/sztuczna-inteligencja/news-wstrzas-w-nauce-openai-i-anthropic-przedstawily-dowody-tego,nId,23565804).** Przekazany przez użytkownika materiał wtórny dotyczący odrębnych ogłoszeń; należy zachować rozróżnienie od sporu o prywatne sesje. Powiązany rozdział: 2.
18. **Fragment przekazany przez użytkownika. Generative Chat at Oracle: Terms of Use & Disclaimer.** Nie przekazano publicznego URL, wersji ani daty obowiązywania. Wykorzystany wyłącznie jako przykład projektowania polityki. Stwierdzenia o zatwierdzeniu przez CSSAP i Oracle Legal, kluczach zarządzanych przez Oracle i dozwolonych kategoriach danych nie zostały niezależnie zweryfikowane i nie potwierdzają równoważnej ochrony w innym wdrożeniu. Powiązany rozdział: 5.

### Konfiguracja lokalna i cykl życia danych

19. **OpenAI. [Podstawy konfiguracji](https://learn.chatgpt.com/docs/config-file/config-basic).** Poziomy konfiguracji, kolejność pierwszeństwa i rozróżnienie ustawień domyślnych od wymuszanych wymagań. Powiązane rozdziały: 6, 13.
20. **OpenAI. [Konfiguracja zaawansowana](https://learn.chatgpt.com/docs/config-file/config-advanced).** Konfiguracja użytkownika, nadpisania projektu i przykłady przechowywania stanu lokalnego oraz poświadczeń. Powiązane rozdziały: 6, 9.
21. **OpenAI. [Zmienne środowiskowe](https://learn.chatgpt.com/docs/config-file/environment-variables).** `CODEX_HOME` i konfigurowalne lokalizacje stanu SQLite. Powiązany rozdział: 6.
22. **OpenAI. [Referencja konfiguracji](https://learn.chatgpt.com/docs/config-file/config-reference).** Obsługiwane klucze i ograniczenia zakresu; ustawień historii nie należy traktować jako globalnej kontroli usuwania. Powiązane rozdziały: 6, 9, 13.
23. **OpenAI. [Instrukcje własne z AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).** Wyszukiwanie instrukcji użytkownika i projektu oraz włączanie ich do kontekstu. Powiązane rozdziały: 6, 12.
24. **OpenAI. [Pamięci](https://learn.chatgpt.com/docs/customization/memories).** Zapis, ponowne wykorzystanie i kontrola pamięci lokalnej Codex, odrębnej od pamięci ChatGPT w przeglądarce. Powiązane rozdziały: 6, 9.
25. **OpenAI. [Diagnostyka](https://learn.chatgpt.com/docs/reference/troubleshooting).** Lokalizacje sesji, archiwów sesji i logów aplikacji; przegląd danych poufnych przed przekazaniem diagnostyki. Powiązane rozdziały: 6, 9, 13.
26. **OpenAI. [Projekty i rozmowy](https://learn.chatgpt.com/docs/projects).** Wspólny kontekst projektu ChatGPT, odrębny od lokalnego repozytorium i stanu Codex. Powiązany rozdział: 6.

### Dodatkowe źródła polityk i umów OpenAI

27. **OpenAI. [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/).** Aktualizacja 1 grudnia 2025 r.; obowiązuje od 1 stycznia 2026 r. Warunki przetwarzania danych osobowych, instrukcje, zgłaszanie naruszeń, warunki audytu i usuwanie. Powiązany rozdział: 4.
28. **OpenAI. [Europe Terms of Use](https://openai.com/policies/eu-terms-of-use/).** Aktualizacja 16 stycznia 2026 r. Warunki usług indywidualnych dla EOG, Szwajcarii i Wielkiej Brytanii; odrębne od umów biznesowych. Powiązany rozdział: 4.
29. **OpenAI. [Europe Privacy Policy](https://openai.com/policies/eu-privacy-policy/).** Aktualizacja 24 sierpnia 2026 r. Informacja o prywatności danych osobowych; wyłącza treści biznesowe przetwarzane w imieniu klienta. Powiązany rozdział: 4.
30. **OpenAI. [Service Terms](https://openai.com/policies/service-terms/).** Aktualizacja 16 października 2026 r. Dodatkowe postanowienia właściwe dla funkcji. Powiązany rozdział: 4.
31. **OpenAI. [Enterprise privacy](https://openai.com/enterprise-privacy/).** Aktualizacja 8 stycznia 2026 r. Opis dostawcy dotyczący ochrony danych biznesowych i dostępu. Powiązany rozdział: 4.
32. **OpenAI. [Lista podwykonawców](https://openai.com/policies/sub-processor-list/).** Aktualizacja 14 października 2026 r. Odbiorcy, zakres usług, cele i lokalizacje przetwarzania. Powiązany rozdział: 4.
33. **OpenAI. [How your data is used to improve model performance](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).** Aktualizacja 13 marca 2026 r. Rozróżnienie treningu dla usług indywidualnych i biznesowych oraz zgody na udostępnianie danych. Powiązany rozdział: 4.
