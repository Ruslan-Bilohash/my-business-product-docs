# My Business Product

**Valdykite visą verslą iš vieno skydelio.**

Savarankiškai talpinamas Laravel 13 + Filament 3.3 administravimo skydelis produktų katalogui, daugiasandėliniam sandėliavimui, sąskaitų išrašymui su realiai veikiančiais mokėjimo šliuzais bei rinkodaros / prekyviečių prijungimais Google, Meta, Amazon, eBay ir kitiems. Vienas pirkinys, diegiate savo serveryje, valdote amžinai — jokie duomenys apie jūsų katalogą, klientus ar API raktus niekada nepraeina per trečiosios šalies serverį.

**Versija 1.32.4** · Administravimo skydelis, vitrina ir dokumentacija pasiekiami 14 kalbų: anglų, ukrainiečių, norvegų, švedų, lietuvių, vokiečių, ispanų, portugalų, Brazilijos portugalų, prancūzų, lenkų, italų, turkų, olandų ir indoneziečių.

---

## Kas viduje

| Modulis | Ką daro |
|---|---|
| **Katalogas ir variantai** | Produktai, variantai, kategorijos, brūkšniniai kodai, pagrindinis vaizdas + pertvarkomi galerijos vaizdai, neprivalomi dokumentai (specifikacijos, brėžiniai). Kiekvienas įkeltas vaizdas automatiškai konvertuojamas į WebP. Masinis CSV importas/eksportas bei realus produktų importas iš Shopify, WooCommerce, Amazon ir eBay — vienas mygtukas, pasirinkite šaltinį |
| **Brūkšninių kodų skenavimas** | Produktų paieška randa prekes pagal nuskenuotą brūkšninį kodą / SKU tiesiogiai; važtaraščių ir užsakymų eilutės turi mygtuką „Skenuoti brūkšninį kodą“ USB/Bluetooth skaitytuvams |
| **Daugiasandėlinis sandėliavimas** | Kiekis stebimas kiekviename sandėlyje, gaunamieji/išsiunčiamieji/perkėlimo važtaraščiai, kiekvienas judėjimas registruojamas automatiškai |
| **Sąskaitos ir mokėjimai** | Firminės sąskaitos su tokenizuota vieša mokėjimo puslapiu ir atsisiunčiamu PDF — 8 aktyvūs mokėjimo šliuzai (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), patvirtinami serverio pusėje per pasirašytus webhook'us |
| **Rinkodara ir prekyvietės** | Gyva katalogo sinchronizacija su Google Shopping ir Meta Catalog; reklamos rezultatai iš Google, Meta ir TikTok Ads; ryšiai su Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop ir Wix |
| **Įmontuotas SEO** | Realus meta description, Open Graph, Twitter Card ir Schema.org JSON-LD išvedimas vitrinoje — ne vien nustatymų laukai. Gyvi `/sitemap.xml` ir `/robots.txt` |
| **AI asistentas** | Naudokite savo Anthropic, OpenAI ar xAI raktą — „Generuoti su AI“ produktų aprašymams / SEO tekstui, taip pat neprivalomas, be būsenos AI pokalbių valdiklis vitrinoje su jūsų parašyta sistemine užklausa |
| **El. paštas, SMS ir Telegram** | Tikslinės kampanijos pagal kainų grupę, taip pat įspėjimai apie mažas atsargas, siunčiami į jūsų pačių Telegram robotą |
| **Vaidmenimis pagrįstas saugumas** | Dviejų veiksnių prisijungimas (TOTP, vietoje generuojamas QR kodas ir atkūrimo kodai), šeši įmontuoti vaidmenys su teisėmis, taikomomis kiekvienam moduliui, pilnas veiklos matomumas |
| **Puslapis „Serveris ir sauga“** | Aplinkos informacija, gyvas saugumo kontrolinis sąrašas, tik localhost prievadų patikra, ir vieno paspaudimo derinimo režimo perjungimas + talpyklos valymas — nereikia SSH ar artisan prieigos |
| **Apsauga nuo srauto perkrovos** | Užklausų dažnio ribojimas kiekviename viešame maršrute; `TRUSTED_PROXIES` palaikymas, kad viskas veiktų teisingai už Cloudflare ar kito CDN/WAF |

Į komplektą įeina ir vieša, klientams skirta **vitrina** — atskira nuo administravimo skydelio, su paieška, filtrais, krepšeliu, apmokėjimu, produkto vaizdų galerija ir neprivalomu AI pokalbių valdikliu.

---

## Ekrano nuotraukos

### Skydelis
![Skydelis](../public/images/tour/dashboard.webp)

### Produktai
![Produktai](../public/images/tour/products.webp)

### Sąskaitos
![Sąskaitos](../public/images/tour/invoices.webp)

### Užsakymai
![Užsakymai](../public/images/tour/orders.webp)

### Vieša vitrina
![Vitrina](../public/images/storefront-preview.webp)

### Rinkodara ir reklama
![Rinkodara](../public/images/features/feature-marketing.webp)

### Prekyvietės
![Prekyvietės](../public/images/features/doc-marketplaces.webp)

### Pranešimai
![Pranešimai](../public/images/features/doc-notifications.webp)

### Naudotojai ir vaidmenys
![Naudotojai](../public/images/features/feature-security.webp)

### Serveris ir sauga
![Serveris ir sauga](../public/images/tour/server-security.webp)

### Prisijungimas
![Prisijungimas](../public/images/screenshot-login.webp)

---

## Technologijos

- **Laravel** 13
- **Filament** 3.3 (administravimo skydelis)
- **PHP** 8.3+
- **MySQL** 8+
- Paprastas Blade vitrinai — jokio kūrimo (build) žingsnio nereikia

## Diegimas

Žiniatinklio diegimo vediklis (`/install`) atlieka reikalavimų patikrą, duomenų bazės nustatymą, migracijas, neprivalomą demonstracinių duomenų užpildymą, pirmosios administratoriaus paskyros ir įmonės duomenų sukūrimą — 14 kalbų, ir veikia nepriklausomai nuo to, ar programa yra domeno šaknyje, ar bet kuriame pakataloge, Apache, LiteSpeed ar nginx serveryje. Žr. `README.txt` ir `public/documentation.html` išsamias diegimo instrukcijas arba diekite rankiniu būdu:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licencija

Privati/komercinė — žr. `LICENSE.txt`. Šis saugykla nėra vieša atvirojo kodo platinama versija.
