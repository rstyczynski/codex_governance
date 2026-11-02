## 13. DLP i ograniczenia działań agentów

DLP analizuje treść w poszukiwaniu określonych informacji wrażliwych, a ograniczenia działań agentów wyznaczają, do jakich informacji i systemów asystent może uzyskać dostęp. Połączenie tych mechanizmów może ograniczyć przypadkowe ujawnienie. Wykrycie rozpoznawalnego sekretu dostępu lub znanego dokumentu trzeba jednak odróżnić od rozpoznania nowego pomysłu biznesowego, który może nie mieć wiarygodnego wzorca umożliwiającego wykrywanie.

**Szkic rozdziału**

- Określenie reguł wykrywania testowych danych uwierzytelniających, danych osobowych, oznaczeń dokumentów, znanych poufnych fragmentów i wzorców charakterystycznych dla firmy.
- Umieszczenie obowiązkowych kontroli danych wejściowych przed przekazaniem do OpenAI. Kontrola odpowiedzi chroni jej późniejsze dostarczenie, a nie poufność promptu, który został już wysłany.
- Przyjęcie blokowania żądania w razie awarii obowiązkowego skanera (fail-closed), z kontrolowaną procedurą wyjątków.
- Określenie zakresu ochrony dla załączników, obrazów, wyników narzędzi, przesyłania strumieniowego, operacji wsadowych i odwołań do wcześniej przesłanych plików. Nieprzetestowane ścieżki pozostają niedopuszczone.
- Ograniczenie dostępu Codex do plików, sieci i narzędzi; traktowanie pobranych instrukcji i treści repozytorium jako potencjalnie niezaufanych.
- Ocena fałszywych alarmów i niewykrytych naruszeń na realistycznych przykładach firmowych.

LiteLLM rozróżnia kontrole przed wywołaniem, po wywołaniu, równoległe i wykonywane wyłącznie na potrzeby logowania. Dla proponowanego wymagania zapobiegania ujawnieniu należy użyć obsługiwanej, blokującej kontroli przed wywołaniem: przy kontroli równoległej żądanie może już trafić do dostawcy, a kontrola wykonywana wyłącznie na potrzeby logowania nie zapobiega ujawnieniu. [Tryby kontroli LiteLLM](https://docs.litellm.ai/docs/proxy/guardrails/quick_start). Dokumentacja zewnętrznych produktów DLP może pomóc określić wymagania, ale obsługa ChatGPT Web nie oznacza automatycznie obsługi Codex lub integracji API. [Macierz obsługi Palo Alto](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).

**Planowany rezultat:** Polityka wykrywania, macierz zakresu ochrony kanałów i dowody, że zablokowana treść testowa nie dotarła do punktu końcowego dostawcy.

