# My Business Product

**Gestiona todo tu negocio desde un solo panel.**

Un panel de administración autoalojado con Laravel 13 + Filament 3.3 para catálogos de productos, inventario multialmacén, facturación con pasarelas de pago realmente funcionales, y conexiones de marketing/marketplaces para Google, Meta, Amazon, eBay y más. Una sola compra, lo instalas en tu propio servidor, lo posees para siempre — nada de tu catálogo, clientes o claves API pasa nunca por un servidor de terceros.

**Versión 1.32.4** · Panel de administración, tienda pública y documentación disponibles en 14 idiomas: inglés, ucraniano, noruego, sueco, lituano, alemán, español, portugués, portugués de Brasil, francés, polaco, italiano, turco, neerlandés e indonesio.

---

## Qué incluye

| Módulo | Qué hace |
|---|---|
| **Catálogo y variantes** | Productos, variantes, categorías, códigos de barras, imagen de portada + imágenes de galería reordenables, documentos opcionales (fichas técnicas, planos, especificaciones). Cada imagen subida se convierte automáticamente a WebP. Importación/exportación masiva por CSV, más importación real de productos desde Shopify, WooCommerce, Amazon y eBay — un botón, elige la fuente |
| **Escaneo de códigos de barras** | La búsqueda de productos encuentra artículos por código de barras/SKU escaneado directamente; las líneas de albaranes y pedidos tienen un botón «Escanear código de barras» para lectores USB/Bluetooth |
| **Inventario multialmacén** | La cantidad se rastrea por almacén, albaranes de entrada/salida/transferencia, cada movimiento se registra automáticamente |
| **Facturas y pagos** | Facturas de marca con una página de pago pública tokenizada y PDF descargable — 8 pasarelas de pago activas (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), verificadas del lado del servidor mediante webhooks firmados |
| **Marketing y marketplaces** | Sincronización de catálogo en vivo con Google Shopping y Meta Catalog; rendimiento publicitario de Google, Meta y TikTok Ads; conexiones para Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop y Wix |
| **SEO integrado** | Salida real de meta description, Open Graph, Twitter Card y Schema.org JSON-LD en la tienda — no solo campos de configuración. `/sitemap.xml` y `/robots.txt` en vivo |
| **Asistente de IA** | Usa tu propia clave de Anthropic, OpenAI o xAI — «Generar con IA» para descripciones de productos/texto SEO, además de un widget de chat de IA opcional y sin estado en la tienda con un prompt de sistema que tú escribes |
| **Email, SMS y Telegram** | Campañas dirigidas por grupo de precios, además de alertas de stock bajo enviadas a tu propio bot de Telegram |
| **Seguridad basada en roles** | Inicio de sesión de dos factores (TOTP, código QR generado localmente y códigos de recuperación), seis roles integrados con permisos aplicados en cada módulo, visibilidad total de la actividad |
| **Página de servidor y seguridad** | Información del entorno, una lista de verificación de seguridad en vivo, una comprobación de puertos solo en localhost, y un interruptor de un clic para el modo de depuración + limpieza de caché — sin necesidad de acceso SSH ni artisan |
| **Protección contra inundaciones** | Limitación de velocidad en cada ruta pública; soporte para `TRUSTED_PROXIES` para que siga funcionando correctamente detrás de Cloudflare u otro CDN/WAF |

También incluye una **tienda** pública orientada al cliente — separada del panel de administración, con búsqueda, filtros, carrito, pago, una galería de imágenes de producto y un widget de chat de IA opcional.

---

## Diseño y UX

**Panel de administración** — Construido sobre Filament 3.3 con una paleta de colores personalizada (azul `#5385C2` como primario, más colores semánticos para peligro/éxito/aviso/información) y la tipografía Inter. Página de inicio de sesión animada en pantalla dividida, un panel en vivo con un gráfico de ingresos de 14 días y una lista de verificación de arranque del negocio, soporte de tema claro/oscuro, y navegación basada en roles — cada uno de los seis roles integrados solo ve los módulos para los que realmente tiene permiso, no simples enlaces en gris inutilizables.

**Tienda pública** — La identidad del tema predeterminado es un aspecto de «manifiesto de transporte» — almacenes, albaranes, niveles de stock — en lugar de una tienda de plantilla genérica: un fondo de papel cálido, texto negro tinta y un color de acento óxido tipo sello, combinados con Big Shoulders Display (titulares), Work Sans (texto corrido) y JetBrains Mono (precios, etiquetas, datos) vía Bunny Fonts — sin Google Fonts, sin rastreo. Una muesca distintiva tipo troquel en el precio (un corte de esquina `clip-path`) se repite en las etiquetas de precio, los sellos de estado y la marca de la cabecera/pie, uniendo todas las páginas. Se incluye un segundo tema, más minimalista, para quienes prefieran un aspecto más sencillo.

**Landing page de marketing** — Una paleta turquesa/azul coherente con el mismo tándem Inter + JetBrains Mono, y un motivo de sello «MANIFEST · MBP-0001» que hace eco de la propia identidad de la tienda, de modo que el sitio de marketing y el producto que vende se sientan como una sola cosa, no dos plantillas sin relación.

**Ningún paso de compilación, en ningún sitio** — Cada pantalla (panel de administración, tienda, páginas de marketing) se entrega con su CSS y JavaScript ya listos. No hay nada que compilar, ninguna dependencia de Node/npm ni ningún framework de CDN que esperar — se descomprime y funciona.

---

## Capturas de pantalla

### Panel principal
![Panel principal](../public/images/tour/dashboard.webp)

### Productos
![Productos](../public/images/tour/products.webp)

### Facturas
![Facturas](../public/images/tour/invoices.webp)

### Pedidos
![Pedidos](../public/images/tour/orders.webp)

### Tienda pública
![Tienda](../public/images/storefront-preview.webp)

### Marketing y anuncios
![Marketing](../public/images/features/feature-marketing.webp)

### Marketplaces
![Marketplaces](../public/images/features/doc-marketplaces.webp)

### Notificaciones
![Notificaciones](../public/images/features/doc-notifications.webp)

### Usuarios y roles
![Usuarios](../public/images/features/feature-security.webp)

### Servidor y seguridad
![Servidor y seguridad](../public/images/tour/server-security.webp)

### Inicio de sesión
![Inicio de sesión](../public/images/screenshot-login.webp)

---

## Tecnología

- **Laravel** 13
- **Filament** 3.3 (panel de administración)
- **PHP** 8.3+
- **MySQL** 8+
- Blade simple para la tienda — no requiere paso de compilación

## Instalación

Un asistente de instalación web (`/install`) gestiona las comprobaciones de requisitos, la configuración de la base de datos, las migraciones, una siembra opcional de datos de demostración, la primera cuenta de administrador y los datos de la empresa — en 14 idiomas, y funciona tanto si la app está en la raíz del dominio como en cualquier subcarpeta, en Apache, LiteSpeed o nginx. Consulta `README.txt` y `public/documentation.html` para las instrucciones completas de configuración, o ejecútalo manualmente:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licencia

Privada/comercial — consulta `LICENSE.txt`. Este repositorio no es una distribución pública de código abierto.
