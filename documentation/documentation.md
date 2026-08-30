# My Business Product

**Run your whole business from one panel.**

A self-hosted Laravel 13 + Filament 3.3 admin panel for product catalogs, multi-warehouse inventory, invoicing with real working payment gateways, and marketing/marketplace connections for Google, Meta, Amazon, eBay and more. One purchase, install it on your own server, own it forever — nothing about your catalog, customers or API keys ever passes through a third-party server.

**Version 1.32.4** · Admin panel, storefront and documentation available in 14 languages: English, Ukrainian, Norwegian, Swedish, Lithuanian, German, Spanish, Portuguese, Brazilian Portuguese, French, Polish, Italian, Turkish, Dutch and Indonesian.

---

## What's inside

| Module | What it does |
|---|---|
| **Catalog & variants** | Products, variants, categories, barcodes, cover + reorderable gallery images, optional documents (datasheets, drawings, specifications). Every uploaded image is auto-converted to WebP. Bulk CSV import/export, plus real product import from Shopify, WooCommerce, Amazon and eBay — one button, pick the source |
| **Barcode scanning** | Product search finds items by scanned barcode/SKU directly; waybill and order line items have a "Scan barcode" button for USB/Bluetooth scanners |
| **Multi-warehouse stock** | Quantity tracked per warehouse, incoming/outgoing/transfer waybills, every movement logged automatically |
| **Invoices & payments** | Branded invoices with a tokenized public payment page and downloadable PDF — 11 live payment gateways (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut, Mollie, Mercado Pago, Midtrans), verified server-side through signed webhooks |
| **Marketing & marketplaces** | Live catalog sync to Google Shopping and Meta Catalog; ad performance from Google, Meta and TikTok Ads; connections for Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop and Wix |
| **News / dispatches** | A built-in news feed — write posts in the admin panel, publish them per-language, and they show up on the public storefront's News section automatically |
| **SEO, built in** | Real meta description, Open Graph, Twitter Card and Schema.org JSON-LD output on the storefront — not just settings fields. Live `/sitemap.xml` and `/robots.txt` |
| **AI assistant** | Bring your own Anthropic, OpenAI or xAI key — "Generate with AI" for product descriptions/SEO text, plus an optional stateless AI chat widget on the storefront using a system prompt you write |
| **Email, SMS & Telegram** | Targeted campaigns by price group, plus low-stock alerts pushed to your own Telegram bot |
| **Role-based security** | Two-factor login (TOTP, locally-generated QR + recovery codes), six built-in roles with permissions enforced on every module, full activity visibility |
| **Server & Security page** | Environment info, a live security checklist, a localhost-only port check, and one-click debug-mode toggle + cache clearing — no SSH or artisan access needed |
| **Flood protection** | Rate limiting on every public route; `TRUSTED_PROXIES` support so it keeps working correctly behind Cloudflare or another CDN/WAF |
| **Security headers** | Every response sends X-Frame-Options, X-Content-Type-Options, Referrer-Policy, a Permissions-Policy and a Content-Security-Policy by default — no configuration needed |

A public, customer-facing **storefront** ships in the box too — separate from the admin panel, with search, filters, cart, checkout, a product image gallery and an optional AI chat widget. The default theme's visual identity is a "trade manifest" look — warehouses, waybills, stock counts — with a signature die-cut price-tag notch, not a generic template shop.

---

## Design & UX

**Admin panel** — Built on Filament 3.3 with a custom color palette (blue `#5385C2` primary, plus semantic colors for danger/success/warning/info) and the Inter typeface. An animated split-screen sign-in page, a live dashboard with a 14-day revenue chart and a business-start checklist, light/dark theme support, and role-based navigation — each of the six built-in roles only sees the modules it actually has permission for, not just greyed-out links it can't use.

**Public storefront** — The default theme's identity is a "trade manifest" look, grounded in the product's own domain (warehouses, waybills, stock counts) rather than a generic template shop: a warm paper background, ink-black text and a rust stamp accent color, paired with Big Shoulders Display (headlines), Work Sans (body text) and JetBrains Mono (prices, labels, data) via Bunny Fonts — no Google Fonts, no tracking. A signature die-cut price-tag notch (a `clip-path` corner cut) repeats across price pills, status stamps and the header/footer brand mark, tying every page together. A second, more minimal theme ships alongside it for buyers who want a plainer look.

**Marketing landing page** — A cohesive teal/blue palette with the same Inter + JetBrains Mono pairing, and a "MANIFEST · MBP-0001" stamp motif that echoes the storefront's own branding, so the marketing site and the product it's selling feel like one thing, not two unrelated templates.

**No build step, anywhere** — Every screen (admin panel, storefront, marketing pages) ships with its CSS and JavaScript already in place. There's nothing to compile, no Node/npm dependency, and no CDN framework to wait on — unzip and it works.

---

## Screenshots

### Dashboard
![Dashboard](../public/images/tour/dashboard.webp)

### Products
![Products](../public/images/tour/products.webp)

### Invoices
![Invoices](../public/images/tour/invoices.webp)

### Orders
![Orders](../public/images/tour/orders.webp)

### Public storefront
![Storefront](../public/images/storefront-preview.webp)

### Marketing & Ads
![Marketing](../public/images/features/feature-marketing.webp)

### Marketplaces
![Marketplaces](../public/images/features/doc-marketplaces.webp)

### Notifications
![Notifications](../public/images/features/doc-notifications.webp)

### Users & roles
![Users](../public/images/features/feature-security.webp)

### Server & Security
![Server & Security](../public/images/tour/server-security.webp)

### Sign in
![Sign in](../public/images/screenshot-login.webp)

---

## Stack

- **Laravel** 13
- **Filament** 3.3 (admin panel)
- **PHP** 8.3+
- **MySQL** 8+
- Plain Blade for the storefront — no build step required

## Installing

A web-based install wizard (`/install`) handles requirements checks, database setup, migrations, an optional demo-data seed, the first admin account and company details — in 14 languages, and works whether the app lives at your domain root or in any subfolder, on Apache, LiteSpeed or nginx. See `README.txt` and `public/documentation.html` for full setup instructions, or run it manually:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## License

Private/commercial — see `LICENSE.txt`. This repository is not a public open-source distribution.
