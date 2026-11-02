## 12. Egzekwowanie reguł sieciowych i OCI Network Firewall

Brama może egzekwować politykę tylko wobec ruchu, który do niej trafia. Proponowana warstwa sieciowa ogranicza więc bezpośredni dostęp z zarządzanych urządzeń i aplikacji, dopuszczając zatwierdzone połączenia bramy do OpenAI. DNS, proxy HTTP i reguły firewalla pełnią uzupełniające role; żadnego z tych mechanizmów nie należy traktować jako samodzielnego, kompletnego rozwiązania.

**Szkic rozdziału**

| Warstwa | Proponowana rola | Granica wymagająca sprawdzenia |
| --- | --- | --- |
| Zarządzany DNS | Ograniczenie niezatwierdzonych nazw i sposobów ich rozwiązywania | Nie analizuje promptów i nie rozróżnia kont w tej samej usłudze |
| Proxy HTTP / Secure Web Gateway | Kontrola obsługiwanego ruchu WWW i inspekcja | Inspekcja HTTPS wymaga zarządzania zaufaniem do certyfikatów i zgodnych aplikacji klienckich |
| Firewall sieciowy | Egzekwowanie dopuszczalnych tras i adresów docelowych ruchu wychodzącego | Obejmuje wyłącznie ruch skierowany przez punkt kontroli |
| Zarządzanie urządzeniami | Utrzymanie zabezpieczeń poza biurem | Wymaga zarządzanych urządzeń i ograniczenia mechanizmów obejścia |

- Inwentaryzacja IPv4, IPv6, alternatywnego i szyfrowanego DNS, tuneli i dostępu spoza sieci firmy.
- Oddzielenie przetwarzania przez model od uwierzytelniania i innych wymaganych połączeń; unikanie ogólnej blokady uniemożliwiającej działanie zatwierdzonej aplikacji.
- Ocena certyfikatów klienckich, zgodności z inspekcją TLS i nieobsługiwanych protokołów bez osłabiania weryfikacji certyfikatów.
- Skierowanie ruchu aplikacji w OCI, a tam, gdzie przewiduje to projekt, także ruchu sieci firmowej przez punkt kontroli.
- Wymaganie zabezpieczeń urządzeń lub dostępu zdalnego dla komputerów pracowników; sam firewall OCI nie obejmuje dowolnych połączeń z laptopów.

OCI Network Firewall jest zarządzanym firewallem Oracle opartym na technologii Palo Alto Networks. Oracle opisuje filtrowanie adresów i URL, wykrywanie i zapobieganie włamaniom oraz inspekcję TLS. Funkcje te nie potwierdzają, że zarządzana usługa OCI obejmuje odrębne produkty Palo Alto Enterprise DLP lub AI Access Security. [Przegląd usługi Oracle](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm). Przykład wdrożenia Secure Web Gateway ilustruje dodatkowe wymagania dotyczące kierowania ruchu i certyfikatów przy inspekcji HTTPS. [Dokumentacja filtrowania HTTP](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).

**Planowany rezultat:** Polityka ruchu wychodzącego, schemat tras, lista wyjątków i wyniki testów obejścia.

