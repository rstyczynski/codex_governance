## 7. Przepływy danych w ChatGPT i Codex

Decyzja dotycząca poufności wymaga pełnego obrazu informacji opuszczających środowisko firmy. Znaczenie ma zarówno sam prompt, jak i załączniki, pobrane dokumenty, fragmenty kodu oraz wyniki narzędzi dodawane do kontekstu modelu. Uruchomienie agenta na firmowym laptopie nie oznacza samo w sobie, że przetwarzanie przez model odbywa się lokalnie.

**Szkic rozdziału**

- Opis przepływu wiadomości, plików, projektów, pamięci, udostępnionych rozmów i połączonych usług ChatGPT, jeśli są włączone.
- Opis przepływu instrukcji, wybranych plików, wyników poleceń, zawartości repozytoriów i zrzutów ekranu w Codex, stosownie do używanych funkcji.
- Rozdzielenie lokalnego wykonywania działań, przetwarzania przez model, wykonywania zadań w chmurze i działania narzędzi podmiotów trzecich.
- Inwentaryzacja danych przechowywanych przez aplikację kliencką, firmowy interfejs rozmowy, bramę, skanery, OpenAI i połączone usługi.
- Określenie granicy między żądaniem do modelu a ruchem pomocniczym, takim jak uwierzytelnianie, wtyczki i wywołania MCP.

Dokumentacja bramy OpenAI wyraźnie wskazuje, że skonfigurowana trasa przez bramę obejmuje żądania do dostawcy modelu, podczas gdy logowanie i inne funkcje mogą korzystać z osobnych ścieżek. To rozróżnienie będzie podstawą inwentaryzacji przepływów. [Dokumentacja bramy OpenAI](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).

**Planowany rezultat:** Schematy przepływu danych wskazujące odbiorców, miejsca przetwarzania i miejsca przechowywania dla każdego zatwierdzonego sposobu pracy.

### 7.1 Poziomy konfiguracji i instrukcje

Codex obsługuje konfigurację systemową, użytkownika i projektu. Jest to hierarchia ustawień, a nie dowód istnienia trzech równoważnych magazynów pamięci podręcznej. W ocenie należy zapisać zarówno zakres ustawienia, jak i fizyczną lokalizację danych, na które ono wpływa.

| Poziom | Przykłady | Pytanie dotyczące poufności |
| --- | --- | --- |
| System / organizacja | `/etc/codex/config.toml` i `/etc/codex/requirements.toml` w systemach Unix; obsługiwane polityki zarządzane | Czy jest to domyślne ustawienie możliwe do nadpisania, czy wymuszane ograniczenie? |
| Użytkownik | `$CODEX_HOME/config.toml`, zwykle `~/.codex/config.toml` | Które projekty dziedziczą dostawców, integracje i ustawienia tego użytkownika? |
| Projekt | Pliki `.codex/config.toml` w zaufanym repozytorium, także w katalogach podrzędnych | Jakie nadpisania obowiązują dla bieżącego katalogu roboczego? |
| Sesja | Flagi CLI i nadpisania podczas uruchomienia | Czy efektywne ustawienia mogą różnić się od sprawdzonego pliku? |

Kolejność pierwszeństwa konfiguracji i wymuszane wymagania to osobne mechanizmy: umieszczenie wartości w systemowym pliku konfiguracji nie czyni jej samo w sobie niezmienną. Warstwy projektu podlegają wymaganiom zaufania i ograniczeniom właściwym dla poszczególnych kluczy. [Podstawy konfiguracji](https://learn.chatgpt.com/docs/config-file/config-basic), [referencja konfiguracji](https://learn.chatgpt.com/docs/config-file/config-reference).

Pliki instrukcji tworzą kolejną warstwę. Pliki `AGENTS.md` użytkownika i projektu mogą wnosić treść do kontekstu modelu; są wskazówkami, a nie zamiennikiem ograniczeń sandboxa lub sieci. [Wyszukiwanie instrukcji](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

### 7.2 Stan lokalny, pamięć podręczna i pliki projektu

`CODEX_HOME` domyślnie wskazuje `~/.codex` i stanowi główny katalog stanu użytkownika. Stan oparty na SQLite można przenieść przez `sqlite_home` lub `CODEX_SQLITE_HOME`. Rzeczywiste ścieżki trzeba więc ustalić dla wybranej aplikacji i hosta. [Zmienne środowiskowe](https://learn.chatgpt.com/docs/config-file/environment-variables).

| Kategoria danych | Lokalizacja lub przykład do zinwentaryzowania | Sposób ujęcia w ocenie |
| --- | --- | --- |
| Dane uwierzytelniające | Plik `auth.json` albo magazyn poświadczeń systemu operacyjnego | Sekrety dostępu, a nie zbędna pamięć podręczna |
| Sesje i historia | `$CODEX_HOME/sessions`, `archived_sessions`; `history.jsonl`, jeśli włączono | Potencjalnie poufne zapisy, odrębne od plików źródłowych projektu |
| Stan wykonania i pamięć podręczna | Skonfigurowana lokalizacja SQLite i katalogi cache właściwe dla aplikacji | Klasyfikacja według rzeczywistej zawartości; bez zakładania, że każdy cache zawiera prompty |
| Pamięć lokalna, jeśli włączona | `$CODEX_HOME/memories` | Informacje pochodne, które mogą wracać w kolejnych rozmowach |
| Pliki projektu i narzędzi | Zmiany w repozytorium, worktree, wygenerowane pliki, wyniki testów i pliki tymczasowe | Ocena przechowywania, dostępu i powielania przez Git lub kopie zapasowe |
| Diagnostyka aplikacji | Lokalizacje logów właściwe dla aplikacji, także poza `CODEX_HOME` | Przegląd przed eksportem lub przekazaniem do wsparcia |

Przykłady przechowywania poświadczeń i stanu użytkownika opisuje [konfiguracja zaawansowana](https://learn.chatgpt.com/docs/config-file/config-advanced); lokalizacje sesji i logów aplikacji wskazuje [dokumentacja diagnostyczna](https://learn.chatgpt.com/docs/reference/troubleshooting). Rozmowa dotycząca projektu może być zapisana w stanie użytkownika: logiczne przypisanie do projektu nie oznacza fizycznego zapisu w jego repozytorium.

Kontekst projektów ChatGPT w przeglądarce i lokalny stan Codex wymagają osobnego opisu. Projekty ChatGPT mogą udostępniać swoim rozmowom pliki i instrukcje. Lokalne pamięci Codex korzystają z osobnego magazynu względem pamięci ChatGPT w przeglądarce; po włączeniu informacje z kwalifikujących się rozmów mogą trafiać do plików pamięci. Ocena poufności między projektami musi więc sprawdzić, czy materiał może powrócić przez wspólne instrukcje użytkownika lub pamięć. [Projekty i rozmowy](https://learn.chatgpt.com/docs/projects), [działanie pamięci](https://learn.chatgpt.com/docs/customization/memories).

**Wymaganie inwentaryzacji:** Dla każdej lokalizacji zapisać właściciela, zawartość, uprawnienia, szyfrowanie, miejsca docelowe kopii lub synchronizacji, możliwość włączenia do kontekstu modelu i procedurę usuwania. W odpowiednim zakresie uwzględnić magazyny przeglądarki i aplikacji zarządzane przez system operacyjny. Lokalny zapis nie dowodzi, że treść nigdy nie zostanie później przesłana; zdalne reguły retencji nie usuwają kopii lokalnych.

