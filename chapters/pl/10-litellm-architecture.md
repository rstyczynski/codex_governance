## 10. Proponowana architektura z LiteLLM

Projekt zakłada wykorzystanie kontrolowanej przez firmę bramy jako punktu wejścia dla zatwierdzonych wywołań modeli OpenAI. LiteLLM jest kandydatem do tej roli i może zostać ograniczone do połączeń z OpenAI. Projekt musi wskazywać, które żądania aplikacji klienckich rzeczywiście przechodzą przez bramę i co następuje, gdy kontrola treści jest niedostępna.

```text
Zarządzane urządzenie użytkownika lub zatwierdzona aplikacja
                         |
    Zatwierdzony interfejs rozmowy lub skonfigurowany Codex
                         |
               Firmowa brama LiteLLM
                         |
       Kontrola treści przed przekazaniem do OpenAI
                         |
          Zatwierdzony punkt końcowy OpenAI
                         |
       Kontrola odpowiedzi przed dostarczeniem użytkownikowi

Zabezpieczenia równoległe:
  - Ograniczenie niezatwierdzonego bezpośredniego dostępu
    do modeli i publicznego interfejsu ChatGPT.
  - Dopuszczenie udokumentowanych połączeń uwierzytelniających
    i pomocniczych w niezbędnym zakresie.
  - Osobna kontrola ruchu narzędzi, wtyczek i MCP.
```

**Szkic rozdziału**

- Rozpoczęcie pilotażu od aplikacji firmowych i Codex CLI skonfigurowanego do zatwierdzonego dostępu do OpenAI API przez LiteLLM.
- Jednoznaczny wybór sposobu uwierzytelniania i rozliczania po stronie OpenAI. Ścieżka abonamentu ChatGPT jest osobnym wariantem projektowym, a nie zakładanym odpowiednikiem dostępu przez klucz API.
- Określenie list dozwolonych modeli, uwierzytelniania użytkowników, danych dostępowych, limitów i kontroli zmian administracyjnych.
- Zapewnienie zatwierdzonego interfejsu rozmowy, jeśli publiczny ChatGPT jest blokowany; interfejs oparty na API nie zapewnia automatycznie tych samych funkcji co ChatGPT.
- Minimalizacja zapisywania treści w logach i pamięci podręcznej; ocena każdego skanera i miejsca docelowego logów jako odbiorcy informacji.
- Testowanie każdej dodatkowej aplikacji klienckiej, funkcji chmurowej i operacji API przed rozszerzeniem zakresu dopuszczenia.

LiteLLM opisuje integrację z Codex CLI. OpenAI również dokumentuje kierowanie ruchu przez bramę i granice tego mechanizmu. Potwierdza to możliwość rozwijania takiego projektu, ale nie pełną obsługę wszystkich aplikacji klienckich i połączeń pomocniczych. [Integracja LiteLLM z Codex](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli), [kierowanie ruchu przez bramę OpenAI](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).

**Planowany rezultat:** Zweryfikowana architektura z inwentaryzacją tras, decyzją o uwierzytelnianiu i jasno wskazanymi lukami w zakresie ochrony.

