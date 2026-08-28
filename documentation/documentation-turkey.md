# My Business Product

**Tüm işletmenizi tek bir panelden yönetin.**

Ürün katalogları, çok depolu envanter, gerçekten çalışan ödeme ağ geçitleriyle faturalandırma ve Google, Meta, Amazon, eBay ve daha fazlası için pazarlama/pazar yeri bağlantıları sunan, kendi sunucunuzda barındırılan bir Laravel 13 + Filament 3.3 yönetim paneli. Tek satın alma, kendi sunucunuza kurun, sonsuza kadar sizin olsun — kataloğunuz, müşterileriniz veya API anahtarlarınızla ilgili hiçbir şey asla üçüncü taraf bir sunucudan geçmez.

**Sürüm 1.21.0** · Yönetim paneli, vitrin ve dokümantasyon 12 dilde mevcuttur: İngilizce, Ukraynaca, Norveççe, İsveççe, Litvanyaca, Almanca, İspanyolca, Portekizce, Fransızca, Lehçe, İtalyanca ve Türkçe.

---

## İçinde neler var

| Modül | Ne yapar |
|---|---|
| **Katalog ve varyantlar** | Ürünler, varyantlar, kategoriler, barkodlar, kapak görseli + sırası değiştirilebilen galeri görselleri, isteğe bağlı belgeler (teknik föyler, çizimler, teknik özellikler). Yüklenen her görsel otomatik olarak WebP'ye dönüştürülür. Toplu CSV içe/dışa aktarma, ayrıca Shopify, WooCommerce, Amazon ve eBay'den gerçek ürün içe aktarma — tek düğme, kaynağı seçin |
| **Barkod tarama** | Ürün arama, taranan barkod/SKU ile ürünleri doğrudan bulur; irsaliye ve sipariş kalemlerinde USB/Bluetooth tarayıcılar için "Barkod tara" düğmesi vardır |
| **Çok depolu envanter** | Miktar her depo için ayrı ayrı izlenir, gelen/giden/transfer irsaliyeleri, her hareket otomatik olarak kaydedilir |
| **Faturalar ve ödemeler** | Belirteç tabanlı genel ödeme sayfası ve indirilebilir PDF ile markalı faturalar — 8 aktif ödeme ağ geçidi (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), imzalı webhook'lar aracılığıyla sunucu tarafında doğrulanır |
| **Pazarlama ve pazar yerleri** | Google Shopping ve Meta Catalog ile canlı katalog senkronizasyonu; Google, Meta ve TikTok Ads'ten reklam performansı; Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop ve Wix için bağlantılar |
| **Yerleşik SEO** | Vitrin de sadece ayar alanları değil, gerçek meta description, Open Graph, Twitter Card ve Schema.org JSON-LD çıktısı. Canlı `/sitemap.xml` ve `/robots.txt` |
| **AI asistanı** | Kendi Anthropic, OpenAI veya xAI anahtarınızı kullanın — ürün açıklamaları/SEO metni için "AI ile oluştur", ayrıca sizin yazdığınız bir sistem istemiyle vitrinde isteğe bağlı, durumsuz bir AI sohbet widget'ı |
| **E-posta, SMS ve Telegram** | Fiyat grubuna göre hedefli kampanyalar, ayrıca kendi Telegram botunuza gönderilen düşük stok uyarıları |
| **Rol tabanlı güvenlik** | İki faktörlü giriş (TOTP, yerel olarak oluşturulan QR kodu ve kurtarma kodları), her modülde uygulanan izinlere sahip altı yerleşik rol, tam etkinlik görünürlüğü |
| **Sunucu ve Güvenlik sayfası** | Ortam bilgileri, canlı bir güvenlik kontrol listesi, yalnızca localhost port kontrolü ve tek tıkla hata ayıklama modu değiştirme + önbellek temizleme — SSH veya artisan erişimine gerek yok |
| **Taşkın koruması** | Her genel rotada hız sınırlama; Cloudflare veya başka bir CDN/WAF arkasında doğru çalışmaya devam etmesi için `TRUSTED_PROXIES` desteği |

Genel, müşteriye yönelik bir **vitrin** de kutunun içinde gelir — yönetim panelinden ayrı, arama, filtreler, sepet, ödeme, bir ürün görsel galerisi ve isteğe bağlı bir AI sohbet widget'ı ile.

---

## Ekran görüntüleri

### Kontrol paneli
![Kontrol paneli](../public/images/tour/dashboard.webp)

### Ürünler
![Ürünler](../public/images/tour/products.webp)

### Faturalar
![Faturalar](../public/images/tour/invoices.webp)

### Siparişler
![Siparişler](../public/images/tour/orders.webp)

### Genel vitrin
![Vitrin](../public/images/storefront-preview.webp)

### Pazarlama ve reklamlar
![Pazarlama](../public/images/features/feature-marketing.webp)

### Pazar yerleri
![Pazar yerleri](../public/images/features/doc-marketplaces.webp)

### Bildirimler
![Bildirimler](../public/images/features/doc-notifications.webp)

### Kullanıcılar ve roller
![Kullanıcılar](../public/images/features/feature-security.webp)

### Sunucu ve Güvenlik
![Sunucu ve Güvenlik](../public/images/tour/server-security.webp)

### Giriş
![Giriş](../public/images/screenshot-login.webp)

---

## Teknoloji

- **Laravel** 13
- **Filament** 3.3 (yönetim paneli)
- **PHP** 8.3+
- **MySQL** 8+
- Vitrin için düz Blade — derleme adımı gerekmez

## Kurulum

Web tabanlı bir kurulum sihirbazı (`/install`) gereksinim kontrollerini, veritabanı kurulumunu, migrasyonları, isteğe bağlı bir demo veri tohumlamayı, ilk yönetici hesabını ve şirket bilgilerini yönetir — 12 dilde, ve uygulama alan adı kökünde ya da herhangi bir alt klasörde olsun, Apache, LiteSpeed veya nginx üzerinde çalışır. Tam kurulum talimatları için `README.txt` ve `public/documentation.html` dosyalarına bakın veya manuel olarak çalıştırın:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Lisans

Özel/ticari — bkz. `LICENSE.txt`. Bu depo genel bir açık kaynak dağıtımı değildir.
