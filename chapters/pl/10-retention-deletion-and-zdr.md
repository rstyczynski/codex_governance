## 10. Przechowywanie, usuwanie i Zero Data Retention

Firma musi odróżniać informacje używane tymczasowo do przygotowania odpowiedzi od danych zachowywanych jako historia, stan aplikacji, materiał do monitorowania lub w związku z obowiązkami prawnymi. Wyłączenie treningu modeli nie rozstrzyga wszystkich tych kwestii, a usunięcie elementu z interfejsu użytkownika nie dowodzi natychmiastowego zniknięcia każdej jego kopii.

**Szkic rozdziału**

- Osobna inwentaryzacja okresów przechowywania dla ChatGPT, Codex, funkcji API, systemów firmowych i integracji zewnętrznych.
- Przegląd procedur usuwania, kopii zapasowych, postępowań dotyczących bezpieczeństwa i obowiązków zachowania danych wynikających z prawa.
- Sprawdzenie dostępności Zero Data Retention (ZDR) i wyłączeń na poziomie modelu, funkcji, punktu końcowego API i projektu.
- Opis lokalizacji przechowywania danych oddzielnie od miejsca ich przetwarzania.
- Określenie zasad dla logów bramy, pamięci podręcznej, materiału dowodowego skanerów i eksportów diagnostycznych.
- Osobna ocena lokalnych sesji, pamięci, baz aplikacji, plików projektu i ich kopii zapasowych. Wyłączenie `history.persistence` dotyczy wskazanej funkcji historii; nie dowodzi wyłączenia wszystkich mechanizmów lokalnego zapisu. Należy sprawdzić każdy magazyn i zakres działania poleceń usuwania. [Referencja konfiguracji](https://learn.chatgpt.com/docs/config-file/config-reference).

Dokumentacja API OpenAI odróżnia logi monitorowania nadużyć od stanu aplikacji, opisuje standardowe okresy przechowywania na potrzeby monitorowania oraz warunki i wyjątki ZDR. Wskazuje też sytuacje, w których przechowywanie na potrzeby bezpieczeństwa może objąć klientów korzystających z tych mechanizmów. Zasad API nie należy uogólniać na wszystkie sposoby korzystania z ChatGPT lub Codex. [Kontrola danych w OpenAI](https://developers.openai.com/api/docs/guides/your-data).

**Planowany rezultat:** Harmonogram przechowywania wskazujący treść, lokalizację, okres, mechanizm usuwania i wyjątki.

