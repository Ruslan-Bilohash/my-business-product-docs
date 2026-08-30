# My Business Product

**Gérez toute votre entreprise depuis un seul panneau.**

Un panneau d'administration auto-hébergé Laravel 13 + Filament 3.3 pour les catalogues de produits, l'inventaire multi-entrepôts, la facturation avec des passerelles de paiement réellement fonctionnelles, et des connexions marketing/marketplaces pour Google, Meta, Amazon, eBay et plus encore. Un seul achat, installez-le sur votre propre serveur, possédez-le pour toujours — rien concernant votre catalogue, vos clients ou vos clés API ne transite jamais par un serveur tiers.

**Version 1.32.4** · Panneau d'administration, boutique et documentation disponibles en 14 langues : anglais, ukrainien, norvégien, suédois, lituanien, allemand, espagnol, portugais, portugais brésilien, français, polonais, italien, turc, néerlandais et indonésien.

---

## Ce qui est inclus

| Module | Ce qu'il fait |
|---|---|
| **Catalogue et variantes** | Produits, variantes, catégories, codes-barres, image de couverture + images de galerie réorganisables, documents optionnels (fiches techniques, plans, spécifications). Chaque image téléchargée est automatiquement convertie en WebP. Import/export CSV en masse, plus import réel de produits depuis Shopify, WooCommerce, Amazon et eBay — un seul bouton, choisissez la source |
| **Scan de codes-barres** | La recherche de produits trouve les articles directement via un code-barres/SKU scanné ; les lignes de bons de livraison et de commandes ont un bouton « Scanner un code-barres » pour les lecteurs USB/Bluetooth |
| **Inventaire multi-entrepôts** | La quantité est suivie par entrepôt, bons de livraison entrants/sortants/de transfert, chaque mouvement est enregistré automatiquement |
| **Factures et paiements** | Factures personnalisées avec une page de paiement publique sécurisée par jeton et un PDF téléchargeable — 8 passerelles de paiement actives (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), vérifiées côté serveur via des webhooks signés |
| **Marketing et marketplaces** | Synchronisation de catalogue en direct avec Google Shopping et Meta Catalog ; performances publicitaires de Google, Meta et TikTok Ads ; connexions pour Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop et Wix |
| **SEO intégré** | Véritable sortie de meta description, Open Graph, Twitter Card et Schema.org JSON-LD sur la boutique — pas seulement des champs de configuration. `/sitemap.xml` et `/robots.txt` en direct |
| **Assistant IA** | Apportez votre propre clé Anthropic, OpenAI ou xAI — « Générer avec l'IA » pour les descriptions de produits/texte SEO, plus un widget de chat IA optionnel et sans état sur la boutique avec une instruction système que vous rédigez |
| **E-mail, SMS et Telegram** | Campagnes ciblées par groupe de prix, plus des alertes de stock faible envoyées vers votre propre bot Telegram |
| **Sécurité basée sur les rôles** | Connexion à deux facteurs (TOTP, QR code généré localement et codes de récupération), six rôles intégrés avec des permissions appliquées sur chaque module, visibilité totale de l'activité |
| **Page Serveur et sécurité** | Informations sur l'environnement, une liste de contrôle de sécurité en direct, une vérification des ports localhost uniquement, et un basculement en un clic du mode débogage + vidage du cache — aucun accès SSH ou artisan nécessaire |
| **Protection contre les inondations** | Limitation de débit sur chaque route publique ; prise en charge de `TRUSTED_PROXIES` afin que tout continue de fonctionner correctement derrière Cloudflare ou un autre CDN/WAF |

Une **boutique** publique orientée client est également incluse — distincte du panneau d'administration, avec recherche, filtres, panier, paiement, une galerie d'images produit et un widget de chat IA optionnel.

---

## Design & UX

**Panneau d'administration** — Construit sur Filament 3.3 avec une palette de couleurs personnalisée (bleu `#5385C2` en primaire, plus des couleurs sémantiques pour danger/succès/avertissement/info) et la police Inter. Page de connexion animée en écran divisé, tableau de bord en direct avec un graphique de revenus sur 14 jours et une checklist de démarrage, prise en charge des thèmes clair/sombre, et navigation basée sur les rôles — chacun des six rôles intégrés ne voit que les modules pour lesquels il a réellement la permission, pas de simples liens grisés inutilisables.

**Boutique publique** — L'identité du thème par défaut est celle d'un « manifeste de transport » — entrepôts, bordereaux d'expédition, niveaux de stock — plutôt qu'une boutique générique de gabarit : un fond papier chaud, un texte noir encre et une couleur d'accent rouille tampon, associés à Big Shoulders Display (titres), Work Sans (texte courant) et JetBrains Mono (prix, étiquettes, données) via Bunny Fonts — sans Google Fonts, sans tracking. Une encoche signature en forme de découpe (un angle en `clip-path`) se répète sur les pastilles de prix, les tampons de statut et la marque de l'en-tête/pied de page, reliant chaque page entre elles. Un second thème, plus minimaliste, est fourni pour les acheteurs qui préfèrent un rendu plus sobre.

**Page d'accueil marketing** — Une palette turquoise/bleu cohérente avec le même duo Inter + JetBrains Mono, et un motif de tampon « MANIFEST · MBP-0001 » qui fait écho à l'identité de la boutique elle-même, pour que le site marketing et le produit qu'il vend se ressentent comme une seule chose, pas deux gabarits sans rapport.

**Aucune étape de build, nulle part** — Chaque écran (panneau d'administration, boutique, pages marketing) est livré avec son CSS et son JavaScript déjà en place. Rien à compiler, aucune dépendance Node/npm, aucun framework CDN à attendre — on décompresse, et ça fonctionne.

---

## Captures d'écran

### Tableau de bord
![Tableau de bord](../public/images/tour/dashboard.webp)

### Produits
![Produits](../public/images/tour/products.webp)

### Factures
![Factures](../public/images/tour/invoices.webp)

### Commandes
![Commandes](../public/images/tour/orders.webp)

### Boutique publique
![Boutique](../public/images/storefront-preview.webp)

### Marketing et publicités
![Marketing](../public/images/features/feature-marketing.webp)

### Marketplaces
![Marketplaces](../public/images/features/doc-marketplaces.webp)

### Notifications
![Notifications](../public/images/features/doc-notifications.webp)

### Utilisateurs et rôles
![Utilisateurs](../public/images/features/feature-security.webp)

### Serveur et sécurité
![Serveur et sécurité](../public/images/tour/server-security.webp)

### Connexion
![Connexion](../public/images/screenshot-login.webp)

---

## Stack technique

- **Laravel** 13
- **Filament** 3.3 (panneau d'administration)
- **PHP** 8.3+
- **MySQL** 8+
- Blade simple pour la boutique — aucune étape de build nécessaire

## Installation

Un assistant d'installation web (`/install`) gère les vérifications des prérequis, la configuration de la base de données, les migrations, un peuplement optionnel de données de démonstration, le premier compte administrateur et les informations de l'entreprise — en 14 langues, et fonctionne que l'application soit à la racine du domaine ou dans n'importe quel sous-dossier, sur Apache, LiteSpeed ou nginx. Consultez `README.txt` et `public/documentation.html` pour les instructions d'installation complètes, ou exécutez-le manuellement :

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licence

Privée/commerciale — voir `LICENSE.txt`. Ce dépôt n'est pas une distribution open source publique.
