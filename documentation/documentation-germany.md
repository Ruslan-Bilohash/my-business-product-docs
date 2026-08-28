# My Business Product

**Führen Sie Ihr gesamtes Unternehmen von einem Panel aus.**

Ein selbstgehostetes Laravel 13 + Filament 3.3 Admin-Panel für Produktkataloge, Lagerbestand über mehrere Lager hinweg, Rechnungsstellung mit echt funktionierenden Zahlungs-Gateways und Marketing-/Marktplatz-Anbindungen für Google, Meta, Amazon, eBay und mehr. Ein Kauf, installieren Sie es auf Ihrem eigenen Server, besitzen Sie es für immer — nichts über Ihren Katalog, Ihre Kunden oder API-Schlüssel läuft jemals über einen Server eines Drittanbieters.

**Version 1.21.0** · Admin-Panel, Storefront und Dokumentation verfügbar in 12 Sprachen: Englisch, Ukrainisch, Norwegisch, Schwedisch, Litauisch, Deutsch, Spanisch, Portugiesisch, Französisch, Polnisch, Italienisch und Türkisch.

---

## Was enthalten ist

| Modul | Was es tut |
|---|---|
| **Katalog & Varianten** | Produkte, Varianten, Kategorien, Barcodes, Titelbild + neu anordenbare Galeriebilder, optionale Dokumente (Datenblätter, Zeichnungen, Spezifikationen). Jedes hochgeladene Bild wird automatisch in WebP konvertiert. Massen-CSV-Import/-Export, plus echter Produktimport von Shopify, WooCommerce, Amazon und eBay — eine Schaltfläche, Quelle auswählen |
| **Barcode-Scannen** | Die Produktsuche findet Artikel direkt über gescannten Barcode/SKU; Wareneingangs- und Bestellpositionen haben eine „Barcode scannen"-Schaltfläche für USB-/Bluetooth-Scanner |
| **Lager über mehrere Standorte** | Menge wird pro Lager verfolgt, Eingangs-/Ausgangs-/Transferbelege, jede Bewegung wird automatisch protokolliert |
| **Rechnungen & Zahlungen** | Gebrandete Rechnungen mit einer tokenbasierten öffentlichen Zahlungsseite und herunterladbarem PDF — 8 aktive Zahlungs-Gateways (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), serverseitig über signierte Webhooks verifiziert |
| **Marketing & Marktplätze** | Live-Katalogsynchronisierung mit Google Shopping und Meta Catalog; Anzeigenleistung von Google, Meta und TikTok Ads; Anbindungen für Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop und Wix |
| **Eingebautes SEO** | Echte Meta-Description-, Open-Graph-, Twitter-Card- und Schema.org-JSON-LD-Ausgabe auf der Storefront — nicht nur Einstellungsfelder. Live `/sitemap.xml` und `/robots.txt` |
| **KI-Assistent** | Bringen Sie Ihren eigenen Anthropic-, OpenAI- oder xAI-Schlüssel mit — „Mit KI generieren" für Produktbeschreibungen/SEO-Text, plus ein optionales, zustandsloses KI-Chat-Widget auf der Storefront mit einem von Ihnen geschriebenen System-Prompt |
| **E-Mail, SMS & Telegram** | Gezielte Kampagnen nach Preisgruppe, plus Benachrichtigungen bei niedrigem Lagerbestand an Ihren eigenen Telegram-Bot |
| **Rollenbasierte Sicherheit** | Zwei-Faktor-Login (TOTP, lokal generierter QR-Code und Wiederherstellungscodes), sechs integrierte Rollen mit Berechtigungen, die auf jedes Modul durchgesetzt werden, volle Aktivitätstransparenz |
| **Seite „Server & Sicherheit"** | Umgebungsinformationen, eine Live-Sicherheitscheckliste, eine reine Localhost-Port-Prüfung sowie Ein-Klick-Umschaltung des Debug-Modus + Cache-Leerung — kein SSH- oder Artisan-Zugriff nötig |
| **Flutschutz** | Rate-Limiting auf jeder öffentlichen Route; `TRUSTED_PROXIES`-Unterstützung, damit alles hinter Cloudflare oder einem anderen CDN/WAF weiterhin korrekt funktioniert |

Eine öffentliche, kundenorientierte **Storefront** ist ebenfalls im Lieferumfang enthalten — getrennt vom Admin-Panel, mit Suche, Filtern, Warenkorb, Checkout, einer Produktbildergalerie und einem optionalen KI-Chat-Widget.

---

## Screenshots

### Dashboard
![Dashboard](../public/images/tour/dashboard.webp)

### Produkte
![Produkte](../public/images/tour/products.webp)

### Rechnungen
![Rechnungen](../public/images/tour/invoices.webp)

### Bestellungen
![Bestellungen](../public/images/tour/orders.webp)

### Öffentliche Storefront
![Storefront](../public/images/storefront-preview.webp)

### Marketing & Werbung
![Marketing](../public/images/features/feature-marketing.webp)

### Marktplätze
![Marktplätze](../public/images/features/doc-marketplaces.webp)

### Benachrichtigungen
![Benachrichtigungen](../public/images/features/doc-notifications.webp)

### Benutzer & Rollen
![Benutzer](../public/images/features/feature-security.webp)

### Server & Sicherheit
![Server & Sicherheit](../public/images/tour/server-security.webp)

### Anmeldung
![Anmeldung](../public/images/screenshot-login.webp)

---

## Technologie

- **Laravel** 13
- **Filament** 3.3 (Admin-Panel)
- **PHP** 8.3+
- **MySQL** 8+
- Einfaches Blade für die Storefront — kein Build-Schritt erforderlich

## Installation

Ein webbasierter Installationsassistent (`/install`) übernimmt Anforderungsprüfungen, Datenbank-Setup, Migrationen, eine optionale Beispieldaten-Seed, das erste Admin-Konto und Firmendaten — in 12 Sprachen, und funktioniert unabhängig davon, ob die App im Domain-Root oder in einem beliebigen Unterordner liegt, auf Apache, LiteSpeed oder nginx. Siehe `README.txt` und `public/documentation.html` für vollständige Einrichtungsanweisungen, oder führen Sie es manuell aus:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Lizenz

Privat/kommerziell — siehe `LICENSE.txt`. Dieses Repository ist keine öffentliche Open-Source-Distribution.
