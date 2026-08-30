# My Business Product — Documentation

**Run your whole business from one panel.**

A self-hosted Laravel 13 + Filament 3.3 admin panel for product catalogs, multi-warehouse inventory, invoicing with real working payment gateways, and marketing/marketplace connections for Google, Meta, Amazon, eBay and more. One purchase, install it on your own server, own it forever — nothing about your catalog, customers or API keys ever passes through a third-party server.

**Current version: 1.32.4**

This repository holds the product's public documentation and screenshots only — it is not the application source code, which is a licensed, commercial product.

**Live demo:** [bilohash.com/laravel/my-business-product](https://bilohash.com/laravel/my-business-product/)

![Dashboard](public/images/tour/dashboard.webp)

---

## Read the full documentation

The full write-up — feature table, design & UX notes, screenshots of every module, tech stack, install instructions — is available in 14 languages:

| Language | Documentation |
|---|---|
| 🇬🇧 English | [documentation/documentation.md](documentation/documentation.md) |
| 🇺🇦 Українська | [documentation/documentation-ukraine.md](documentation/documentation-ukraine.md) |
| 🇳🇴 Norsk | [documentation/documentation-norway.md](documentation/documentation-norway.md) |
| 🇸🇪 Svenska | [documentation/documentation-sweden.md](documentation/documentation-sweden.md) |
| 🇱🇹 Lietuvių | [documentation/documentation-lithuania.md](documentation/documentation-lithuania.md) |
| 🇩🇪 Deutsch | [documentation/documentation-germany.md](documentation/documentation-germany.md) |
| 🇪🇸 Español | [documentation/documentation-spain.md](documentation/documentation-spain.md) |
| 🇵🇹 Português | [documentation/documentation-portugal.md](documentation/documentation-portugal.md) |
| 🇫🇷 Français | [documentation/documentation-france.md](documentation/documentation-france.md) |
| 🇵🇱 Polski | [documentation/documentation-poland.md](documentation/documentation-poland.md) |
| 🇮🇹 Italiano | [documentation/documentation-italy.md](documentation/documentation-italy.md) |
| 🇹🇷 Türkçe | [documentation/documentation-turkey.md](documentation/documentation-turkey.md) |

The admin panel, storefront and in-app documentation also ship in Brazilian Portuguese, Dutch and Indonesian — those three don't have a standalone write-up in this repo yet, but are fully supported in the product itself.

---

## What's inside, at a glance

- **Catalog & variants** — products, variants, categories, barcodes, cover + gallery images (auto-converted to WebP), optional documents, bulk CSV import/export, and real product import from Shopify, WooCommerce, Amazon and eBay
- **Barcode scanning** — searchable catalog, plus a "Scan barcode" button on waybill and order line items for USB/Bluetooth scanners
- **Multi-warehouse stock** with full movement history
- **Invoices & payments** — 11 live payment gateways, a public tokenized payment page, downloadable PDF
- **Marketing & marketplaces** — Google Shopping, Meta Catalog, Google/Meta/TikTok Ads, Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop, Wix
- **News/dispatches** — a built-in, multi-language news feed on the public storefront
- **Real SEO output** — meta tags, Open Graph, Twitter Card, Schema.org JSON-LD, live sitemap.xml/robots.txt
- **AI assistant** — bring your own API key for AI-generated product/SEO text, plus an optional storefront chat widget
- **Role-based security** — two-factor login, six built-in roles, a Server & Security page with a live checklist and one-click debug/cache controls
- **Standard HTTP security headers** on every response by default (CSP, X-Frame-Options and more)
- **Built-in flood protection** on every public route

A public, customer-facing **storefront** ships in the box too — separate from the admin panel, with search, filters, cart, checkout, a product image gallery and the optional AI chat widget.

---

## Design & UX

The admin panel runs on Filament 3.3 with a custom blue color palette and the Inter typeface — an animated split-screen sign-in, a live dashboard, and navigation that only ever shows a role the modules it's actually permitted to use.

The public storefront's default theme has its own distinct identity: a "trade manifest" look grounded in the product's own domain (warehouses, waybills, stock counts) — warm paper background, ink-black text, a rust stamp accent, and a typeface trio (Big Shoulders Display, Work Sans, JetBrains Mono) via Bunny Fonts, no Google Fonts or tracking. A signature die-cut price-tag notch repeats across price pills, status stamps and the brand mark, and the same "MANIFEST" stamp motif carries through to the marketing landing page, so the two feel like one product. A second, more minimal storefront theme ships alongside it. Every screen ships with its CSS and JavaScript already in place — no Node/npm build step, anywhere.

See the full [Design & UX section](documentation/documentation.md#design--ux) in the documentation for details.

---

## License

This documentation is provided for informational purposes to preview the product. The application itself is a commercial, licensed product — see the listing for licensing terms. This repository does not grant any rights to the source code.
