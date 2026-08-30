# My Business Product

**Prowadź cały swój biznes z jednego panelu.**

Samodzielnie hostowany panel administracyjny Laravel 13 + Filament 3.3 do katalogów produktów, wielomagazynowego zarządzania stanem, fakturowania z naprawdę działającymi bramkami płatności oraz połączeń marketingowych/rynkowych z Google, Meta, Amazon, eBay i innymi. Jeden zakup, instalujesz na własnym serwerze, posiadasz na zawsze — żadne dane o Twoim katalogu, klientach czy kluczach API nigdy nie przechodzą przez serwer strony trzeciej.

**Wersja 1.32.4** · Panel administracyjny, witryna i dokumentacja dostępne w 14 językach: angielskim, ukraińskim, norweskim, szwedzkim, litewskim, niemieckim, hiszpańskim, portugalskim, brazylijskim portugalskim, francuskim, polskim, włoskim, tureckim, niderlandzkim i indonezyjskim.

---

## Co w środku

| Moduł | Co robi |
|---|---|
| **Katalog i warianty** | Produkty, warianty, kategorie, kody kreskowe, zdjęcie główne + zdjęcia galerii z możliwością zmiany kolejności, opcjonalne dokumenty (karty katalogowe, rysunki, specyfikacje). Każde przesłane zdjęcie jest automatycznie konwertowane do WebP. Masowy import/eksport CSV, plus rzeczywisty import produktów z Shopify, WooCommerce, Amazon i eBay — jeden przycisk, wybierz źródło |
| **Skanowanie kodów kreskowych** | Wyszukiwanie produktów znajduje pozycje bezpośrednio po zeskanowanym kodzie kreskowym/SKU; pozycje dokumentów magazynowych i zamówień mają przycisk „Skanuj kod kreskowy” dla czytników USB/Bluetooth |
| **Zarządzanie wieloma magazynami** | Ilość jest śledzona dla każdego magazynu, dokumenty przychodzące/wychodzące/przesunięcia, każdy ruch jest rejestrowany automatycznie |
| **Faktury i płatności** | Markowe faktury z tokenizowaną publiczną stroną płatności i pobieralnym PDF — 8 aktywnych bramek płatności (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), weryfikowanych po stronie serwera za pomocą podpisanych webhooków |
| **Marketing i platformy handlowe** | Synchronizacja katalogu na żywo z Google Shopping i Meta Catalog; wyniki reklam z Google, Meta i TikTok Ads; połączenia z Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop i Wix |
| **Wbudowane SEO** | Prawdziwe dane wyjściowe meta description, Open Graph, Twitter Card i Schema.org JSON-LD w witrynie — nie tylko pola ustawień. Aktywne `/sitemap.xml` i `/robots.txt` |
| **Asystent AI** | Użyj własnego klucza Anthropic, OpenAI lub xAI — „Generuj z AI” dla opisów produktów/tekstu SEO, a także opcjonalny, bezstanowy widżet czatu AI w witrynie z promptem systemowym, który sam napiszesz |
| **E-mail, SMS i Telegram** | Ukierunkowane kampanie według grupy cenowej, a także alerty o niskim stanie magazynowym wysyłane do własnego bota Telegram |
| **Bezpieczeństwo oparte na rolach** | Logowanie dwuskładnikowe (TOTP, lokalnie generowany kod QR i kody odzyskiwania), sześć wbudowanych ról z uprawnieniami egzekwowanymi w każdym module, pełna widoczność aktywności |
| **Strona Serwer i bezpieczeństwo** | Informacje o środowisku, aktywna lista kontrolna bezpieczeństwa, sprawdzanie portów tylko na localhost oraz jednoklikowe przełączanie trybu debugowania + czyszczenie pamięci podręcznej — bez potrzeby dostępu SSH czy artisan |
| **Ochrona przed zalewem ruchu** | Ograniczanie liczby żądań na każdej publicznej trasie; obsługa `TRUSTED_PROXIES`, aby wszystko nadal działało poprawnie za Cloudflare lub innym CDN/WAF |

W zestawie znajduje się także publiczna **witryna** skierowana do klientów — oddzielna od panelu administracyjnego, z wyszukiwaniem, filtrami, koszykiem, płatnością, galerią zdjęć produktu i opcjonalnym widżetem czatu AI.

---

## Design i UX

**Panel administracyjny** — Zbudowany na Filament 3.3 z niestandardową paletą kolorów (niebieski `#5385C2` jako główny, plus kolory semantyczne dla błędu/sukcesu/ostrzeżenia/informacji) i krojem Inter. Animowany ekran logowania podzielony na pół, żywy pulpit z wykresem przychodów z 14 dni i listą kontrolną startu biznesu, obsługa jasnego/ciemnego motywu oraz nawigacja oparta na rolach — każda z sześciu wbudowanych ról widzi tylko moduły, do których faktycznie ma uprawnienia, a nie wyszarzone, bezużyteczne linki.

**Publiczna witryna** — Tożsamość domyślnego motywu to wygląd „manifestu transportowego" — magazyny, listy przewozowe, stany magazynowe — zamiast typowego szablonowego sklepu: ciepłe papierowe tło, atramentowo czarny tekst i rdzawy akcent pieczątki, w połączeniu z Big Shoulders Display (nagłówki), Work Sans (tekst główny) i JetBrains Mono (ceny, etykiety, dane) przez Bunny Fonts — bez Google Fonts, bez śledzenia. Charakterystyczne wycięcie w stylu sztancowania przy cenie (narożne cięcie `clip-path`) powtarza się na pigułkach cenowych, pieczątkach statusu oraz znaku marki w nagłówku/stopce, łącząc wszystkie strony. Drugi, bardziej minimalistyczny motyw jest dołączony dla kupujących, którzy wolą prostszy wygląd.

**Marketingowa strona docelowa** — Spójna paleta turkusowo-niebieska z tym samym zestawieniem Inter + JetBrains Mono oraz motyw pieczątki „MANIFEST · MBP-0001", nawiązujący do tożsamości samej witryny, dzięki czemu strona marketingowa i sprzedawany przez nią produkt sprawiają wrażenie jednej całości, a nie dwóch niepowiązanych szablonów.

**Żadnego kroku budowania, nigdzie** — Każdy ekran (panel administracyjny, witryna, strony marketingowe) jest dostarczany z gotowym już CSS i JavaScript. Nie ma nic do skompilowania, żadnej zależności od Node/npm i żadnego frameworka CDN, na który trzeba czekać — rozpakowujesz i działa.

---

## Zrzuty ekranu

### Pulpit
![Pulpit](../public/images/tour/dashboard.webp)

### Produkty
![Produkty](../public/images/tour/products.webp)

### Faktury
![Faktury](../public/images/tour/invoices.webp)

### Zamówienia
![Zamówienia](../public/images/tour/orders.webp)

### Publiczna witryna
![Witryna](../public/images/storefront-preview.webp)

### Marketing i reklamy
![Marketing](../public/images/features/feature-marketing.webp)

### Platformy handlowe
![Platformy handlowe](../public/images/features/doc-marketplaces.webp)

### Powiadomienia
![Powiadomienia](../public/images/features/doc-notifications.webp)

### Użytkownicy i role
![Użytkownicy](../public/images/features/feature-security.webp)

### Serwer i bezpieczeństwo
![Serwer i bezpieczeństwo](../public/images/tour/server-security.webp)

### Logowanie
![Logowanie](../public/images/screenshot-login.webp)

---

## Technologia

- **Laravel** 13
- **Filament** 3.3 (panel administracyjny)
- **PHP** 8.3+
- **MySQL** 8+
- Zwykły Blade dla witryny — bez etapu budowania

## Instalacja

Internetowy kreator instalacji (`/install`) obsługuje sprawdzanie wymagań, konfigurację bazy danych, migracje, opcjonalne zasilenie danymi demonstracyjnymi, pierwsze konto administratora i dane firmy — w 14 językach, i działa niezależnie od tego, czy aplikacja znajduje się w katalogu głównym domeny, czy w dowolnym podkatalogu, na Apache, LiteSpeed lub nginx. Zobacz `README.txt` i `public/documentation.html`, aby uzyskać pełne instrukcje konfiguracji, lub zainstaluj ręcznie:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licencja

Prywatna/komercyjna — zobacz `LICENSE.txt`. To repozytorium nie jest publiczną dystrybucją open source.
