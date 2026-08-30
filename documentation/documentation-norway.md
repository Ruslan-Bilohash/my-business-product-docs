# My Business Product

**Driv hele virksomheten din fra ett panel.**

Et selvhostet Laravel 13 + Filament 3.3-adminpanel for produktkataloger, lager på tvers av flere lagre, fakturering med ekte fungerende betalingsløsninger, og markedsførings-/markedsplasstilkoblinger for Google, Meta, Amazon, eBay og mer. Ett kjøp, installer det på din egen server, eie det for alltid — ingenting om katalogen, kundene eller API-nøklene dine går noensinne gjennom en tredjepartsserver.

**Versjon 1.32.4** · Admin-panel, nettbutikk og dokumentasjon tilgjengelig på 14 språk: engelsk, ukrainsk, norsk, svensk, litauisk, tysk, spansk, portugisisk, brasiliansk portugisisk, fransk, polsk, italiensk, tyrkisk, nederlandsk og indonesisk.

---

## Hva som er inni

| Modul | Hva den gjør |
|---|---|
| **Katalog og varianter** | Produkter, varianter, kategorier, strekkoder, hovedbilde + omorganiserbare galleribilder, valgfrie dokumenter (datablad, tegninger, spesifikasjoner). Hvert opplastede bilde konverteres automatisk til WebP. Bulk CSV-import/eksport, pluss ekte produktimport fra Shopify, WooCommerce, Amazon og eBay — én knapp, velg kilde |
| **Strekkodeskanning** | Produktsøk finner varer via skannet strekkode/SKU direkte; vare- og ordrelinjer har en «Skann strekkode»-knapp for USB-/Bluetooth-skannere |
| **Lager på tvers av flere lagre** | Antall spores per lager, innkommende/utgående/overførings-fraktbrev, hver bevegelse logges automatisk |
| **Fakturaer og betalinger** | Merkede fakturaer med en tokenbasert offentlig betalingsside og nedlastbar PDF — 8 aktive betalingsløsninger (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), verifisert server-side via signerte webhooks |
| **Markedsføring og markedsplasser** | Live katalogsynkronisering til Google Shopping og Meta Catalog; annonseytelse fra Google, Meta og TikTok Ads; tilkoblinger for Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop og Wix |
| **Innebygd SEO** | Ekte meta description, Open Graph, Twitter Card og Schema.org JSON-LD-utdata på nettbutikken — ikke bare innstillingsfelter. Live `/sitemap.xml` og `/robots.txt` |
| **AI-assistent** | Bruk din egen Anthropic-, OpenAI- eller xAI-nøkkel — «Generer med AI» for produktbeskrivelser/SEO-tekst, pluss en valgfri, tilstandsløs AI-chat-widget på nettbutikken med en systemprompt du selv skriver |
| **E-post, SMS og Telegram** | Målrettede kampanjer etter prisgruppe, pluss varsler om lav lagerbeholdning sendt til din egen Telegram-bot |
| **Rollebasert sikkerhet** | Tofaktorpålogging (TOTP, lokalt generert QR-kode og gjenopprettingskoder), seks innebygde roller med tillatelser håndhevet på hver modul, full aktivitetsinnsyn |
| **Server & sikkerhet-side** | Miljøinformasjon, en live sikkerhetssjekkliste, en localhost-only portsjekk, og ettrykks feilsøkingsmodus-veksling + cache-tømming — ingen SSH eller artisan-tilgang nødvendig |
| **Flombeskyttelse** | Hastighetsbegrensning på hver offentlig rute; støtte for `TRUSTED_PROXIES` slik at det fortsetter å fungere korrekt bak Cloudflare eller en annen CDN/WAF |

En offentlig, kundevendt **nettbutikk** følger også med i esken — separat fra adminpanelet, med søk, filtre, handlekurv, kasse, et produktbildegalleri og en valgfri AI-chat-widget.

---

## Design og UX

**Adminpanel** — Bygget på Filament 3.3 med en tilpasset fargepalett (blå `#5385C2` som primærfarge, pluss semantiske farger for fare/suksess/advarsel/info) og skrifttypen Inter. Animert delt-skjerm-innloggingsside, et live dashbord med et 14-dagers inntektsdiagram og en oppstartssjekkliste, støtte for lyst/mørkt tema, og rollebasert navigasjon — hver av de seks innebygde rollene ser bare modulene den faktisk har tillatelse til, ikke bare grå, ubrukelige lenker.

**Offentlig nettbutikk** — Standardtemaets identitet er et «fraktmanifest»-utseende — lagre, fraktbrev, lagerbeholdning — i stedet for en generisk mal-butikk: en varm papirbakgrunn, blekksvart tekst og en rustfarget stempelaksent, kombinert med Big Shoulders Display (overskrifter), Work Sans (brødtekst) og JetBrains Mono (priser, etiketter, data) via Bunny Fonts — ingen Google Fonts, ingen sporing. Et signaturhakk i utstanset stil på prisen (et hjørnekutt med `clip-path`) gjentas på prislapper, statusstempler og merket i header/footer, og binder hver side sammen. Et andre, mer minimalistisk tema følger med for kjøpere som ønsker et enklere utseende.

**Markedsførings-landingsside** — En helhetlig turkis/blå palett med samme Inter + JetBrains Mono-kombinasjon, og et «MANIFEST · MBP-0001»-stempelmotiv som gjenspeiler nettbutikkens egen merkevarebygging, slik at markedsføringssiden og produktet den selger føles som én ting, ikke to urelaterte maler.

**Ingen byggetrinn, noe sted** — Hver skjerm (adminpanel, nettbutikk, markedsføringssider) leveres med CSS og JavaScript allerede på plass. Det er ingenting å kompilere, ingen Node/npm-avhengighet, og ingen CDN-rammeverk å vente på — pakk ut, og det fungerer.

---

## Skjermbilder

### Dashbord
![Dashbord](../public/images/tour/dashboard.webp)

### Produkter
![Produkter](../public/images/tour/products.webp)

### Fakturaer
![Fakturaer](../public/images/tour/invoices.webp)

### Ordrer
![Ordrer](../public/images/tour/orders.webp)

### Offentlig nettbutikk
![Nettbutikk](../public/images/storefront-preview.webp)

### Markedsføring og annonser
![Markedsføring](../public/images/features/feature-marketing.webp)

### Markedsplasser
![Markedsplasser](../public/images/features/doc-marketplaces.webp)

### Varsler
![Varsler](../public/images/features/doc-notifications.webp)

### Brukere og roller
![Brukere](../public/images/features/feature-security.webp)

### Server & sikkerhet
![Server & sikkerhet](../public/images/tour/server-security.webp)

### Innlogging
![Innlogging](../public/images/screenshot-login.webp)

---

## Teknologi

- **Laravel** 13
- **Filament** 3.3 (adminpanel)
- **PHP** 8.3+
- **MySQL** 8+
- Vanlig Blade for nettbutikken — ingen byggesteg nødvendig

## Installasjon

En nettbasert installasjonsveiviser (`/install`) håndterer kravsjekker, databaseoppsett, migreringer, en valgfri eksempeldata-seed, den første admin-kontoen og firmaopplysninger — på 14 språk, og fungerer enten appen ligger i domenets rot eller i en hvilken som helst undermappe, på Apache, LiteSpeed eller nginx. Se `README.txt` og `public/documentation.html` for fullstendige oppsettinstruksjoner, eller kjør det manuelt:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Lisens

Privat/kommersiell — se `LICENSE.txt`. Dette repositoriet er ikke en offentlig open source-distribusjon.
