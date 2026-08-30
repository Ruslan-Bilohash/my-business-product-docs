# My Business Product

**Gestisci tutta la tua attività da un unico pannello.**

Un pannello di amministrazione autogestito Laravel 13 + Filament 3.3 per cataloghi di prodotti, inventario multi-magazzino, fatturazione con gateway di pagamento realmente funzionanti, e connessioni di marketing/marketplace per Google, Meta, Amazon, eBay e altro ancora. Un solo acquisto, lo installi sul tuo server, lo possiedi per sempre — nulla del tuo catalogo, dei tuoi clienti o delle tue chiavi API passa mai attraverso un server di terze parti.

**Versione 1.32.4** · Pannello di amministrazione, storefront e documentazione disponibili in 14 lingue: inglese, ucraino, norvegese, svedese, lituano, tedesco, spagnolo, portoghese, portoghese brasiliano, francese, polacco, italiano, turco, olandese e indonesiano.

---

## Cosa include

| Modulo | Cosa fa |
|---|---|
| **Catalogo e varianti** | Prodotti, varianti, categorie, codici a barre, immagine di copertina + immagini della galleria riordinabili, documenti opzionali (schede tecniche, disegni, specifiche). Ogni immagine caricata viene automaticamente convertita in WebP. Importazione/esportazione CSV di massa, più importazione reale di prodotti da Shopify, WooCommerce, Amazon ed eBay — un pulsante, scegli la fonte |
| **Scansione codici a barre** | La ricerca prodotti trova gli articoli direttamente tramite codice a barre/SKU scansionato; le righe di bolle di consegna e ordini hanno un pulsante "Scansiona codice a barre" per lettori USB/Bluetooth |
| **Inventario multi-magazzino** | La quantità è tracciata per magazzino, bolle in entrata/uscita/trasferimento, ogni movimento viene registrato automaticamente |
| **Fatture e pagamenti** | Fatture personalizzate con una pagina di pagamento pubblica tokenizzata e PDF scaricabile — 8 gateway di pagamento attivi (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), verificati lato server tramite webhook firmati |
| **Marketing e marketplace** | Sincronizzazione live del catalogo con Google Shopping e Meta Catalog; prestazioni degli annunci di Google, Meta e TikTok Ads; connessioni per Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop e Wix |
| **SEO integrato** | Vera generazione di meta description, Open Graph, Twitter Card e Schema.org JSON-LD sullo storefront — non solo campi di configurazione. `/sitemap.xml` e `/robots.txt` live |
| **Assistente AI** | Usa la tua chiave Anthropic, OpenAI o xAI — "Genera con AI" per descrizioni prodotto/testo SEO, più un widget di chat AI opzionale e senza stato sullo storefront con un prompt di sistema scritto da te |
| **Email, SMS e Telegram** | Campagne mirate per gruppo di prezzo, più avvisi di scorte basse inviati al tuo bot Telegram |
| **Sicurezza basata sui ruoli** | Accesso a due fattori (TOTP, codice QR generato localmente e codici di recupero), sei ruoli integrati con permessi applicati su ogni modulo, piena visibilità delle attività |
| **Pagina Server e sicurezza** | Informazioni sull'ambiente, una checklist di sicurezza live, un controllo delle porte solo su localhost, e un interruttore a un clic per la modalità debug + pulizia della cache — nessun accesso SSH o artisan necessario |
| **Protezione anti-flood** | Limitazione della frequenza su ogni rotta pubblica; supporto per `TRUSTED_PROXIES` in modo che tutto continui a funzionare correttamente dietro Cloudflare o un altro CDN/WAF |

È incluso anche uno **storefront** pubblico rivolto ai clienti — separato dal pannello di amministrazione, con ricerca, filtri, carrello, checkout, una galleria di immagini prodotto e un widget di chat AI opzionale.

---

## Screenshot

### Dashboard
![Dashboard](../public/images/tour/dashboard.webp)

### Prodotti
![Prodotti](../public/images/tour/products.webp)

### Fatture
![Fatture](../public/images/tour/invoices.webp)

### Ordini
![Ordini](../public/images/tour/orders.webp)

### Storefront pubblico
![Storefront](../public/images/storefront-preview.webp)

### Marketing e annunci
![Marketing](../public/images/features/feature-marketing.webp)

### Marketplace
![Marketplace](../public/images/features/doc-marketplaces.webp)

### Notifiche
![Notifiche](../public/images/features/doc-notifications.webp)

### Utenti e ruoli
![Utenti](../public/images/features/feature-security.webp)

### Server e sicurezza
![Server e sicurezza](../public/images/tour/server-security.webp)

### Accesso
![Accesso](../public/images/screenshot-login.webp)

---

## Stack tecnologico

- **Laravel** 13
- **Filament** 3.3 (pannello di amministrazione)
- **PHP** 8.3+
- **MySQL** 8+
- Blade semplice per lo storefront — nessun passaggio di build richiesto

## Installazione

Una procedura guidata di installazione web (`/install`) gestisce i controlli dei requisiti, la configurazione del database, le migrazioni, un seeding opzionale di dati dimostrativi, il primo account amministratore e i dati aziendali — in 14 lingue, e funziona sia che l'app risieda nella root del dominio sia in qualsiasi sottocartella, su Apache, LiteSpeed o nginx. Consulta `README.txt` e `public/documentation.html` per le istruzioni complete di configurazione, oppure eseguila manualmente:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licenza

Privata/commerciale — vedi `LICENSE.txt`. Questo repository non è una distribuzione open source pubblica.
