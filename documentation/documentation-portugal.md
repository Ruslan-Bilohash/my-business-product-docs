# My Business Product

**Geria todo o seu negócio a partir de um único painel.**

Um painel de administração autoalojado em Laravel 13 + Filament 3.3 para catálogos de produtos, inventário multi-armazém, faturação com gateways de pagamento verdadeiramente funcionais, e ligações de marketing/marketplaces para Google, Meta, Amazon, eBay e mais. Uma compra, instala no seu próprio servidor, é seu para sempre — nada sobre o seu catálogo, clientes ou chaves de API passa alguma vez por um servidor de terceiros.

**Versão 1.32.4** · Painel de administração, loja pública e documentação disponíveis em 14 idiomas: inglês, ucraniano, norueguês, sueco, lituano, alemão, espanhol, português, português do Brasil, francês, polaco, italiano, turco, neerlandês e indonésio.

---

## O que está incluído

| Módulo | O que faz |
|---|---|
| **Catálogo e variantes** | Produtos, variantes, categorias, códigos de barras, imagem de capa + imagens de galeria reordenáveis, documentos opcionais (fichas técnicas, desenhos, especificações). Cada imagem carregada é automaticamente convertida para WebP. Importação/exportação em massa via CSV, mais importação real de produtos do Shopify, WooCommerce, Amazon e eBay — um botão, escolha a origem |
| **Leitura de códigos de barras** | A pesquisa de produtos encontra artigos por código de barras/SKU lido diretamente; as linhas de guias de remessa e encomendas têm um botão «Digitalizar código de barras» para leitores USB/Bluetooth |
| **Inventário multi-armazém** | A quantidade é rastreada por armazém, guias de remessa de entrada/saída/transferência, cada movimento é registado automaticamente |
| **Faturas e pagamentos** | Faturas personalizadas com uma página de pagamento pública tokenizada e PDF para transferir — 8 gateways de pagamento ativos (Stripe, PayPal, LiqPay, Fondy, WayForPay, Vipps MobilePay, Paysera, Revolut), verificados no servidor através de webhooks assinados |
| **Marketing e marketplaces** | Sincronização de catálogo em tempo real com Google Shopping e Meta Catalog; desempenho de anúncios do Google, Meta e TikTok Ads; ligações para Amazon, eBay, Rozetka, Shopify, WooCommerce, PrestaShop e Wix |
| **SEO incorporado** | Saída real de meta description, Open Graph, Twitter Card e Schema.org JSON-LD na loja — não apenas campos de configuração. `/sitemap.xml` e `/robots.txt` em tempo real |
| **Assistente de IA** | Traga a sua própria chave Anthropic, OpenAI ou xAI — «Gerar com IA» para descrições de produtos/texto SEO, além de um widget de chat de IA opcional e sem estado na loja com um prompt de sistema escrito por si |
| **Email, SMS e Telegram** | Campanhas direcionadas por grupo de preços, além de alertas de stock baixo enviados para o seu próprio bot do Telegram |
| **Segurança baseada em funções** | Início de sessão de dois fatores (TOTP, código QR gerado localmente e códigos de recuperação), seis funções incorporadas com permissões aplicadas em cada módulo, visibilidade total da atividade |
| **Página Servidor e Segurança** | Informação do ambiente, uma lista de verificação de segurança em tempo real, uma verificação de portas apenas em localhost, e um interruptor de um clique para o modo de depuração + limpeza de cache — sem necessidade de acesso SSH ou artisan |
| **Proteção contra inundações** | Limitação de taxa em cada rota pública; suporte para `TRUSTED_PROXIES` para que continue a funcionar corretamente atrás do Cloudflare ou de outro CDN/WAF |

Uma **loja** pública voltada para o cliente também está incluída — separada do painel de administração, com pesquisa, filtros, carrinho, checkout, uma galeria de imagens de produto e um widget de chat de IA opcional.

---

## Design e UX

**Painel de administração** — Construído sobre o Filament 3.3 com uma paleta de cores personalizada (azul `#5385C2` como primária, mais cores semânticas para perigo/sucesso/aviso/informação) e o tipo de letra Inter. Página de início de sessão animada em ecrã dividido, um painel ao vivo com um gráfico de receita de 14 dias e uma checklist de arranque do negócio, suporte para tema claro/escuro, e navegação baseada em funções — cada uma das seis funções incluídas só vê os módulos para os quais tem, de facto, permissão, e não meras ligações acinzentadas e inutilizáveis.

**Loja pública** — A identidade do tema predefinido é um aspeto de «manifesto de transporte» — armazéns, guias de remessa, níveis de stock — em vez de uma loja genérica de modelo: um fundo em papel quente, texto preto tinta e um acento cor de ferrugem de carimbo, combinados com Big Shoulders Display (títulos), Work Sans (texto corrido) e JetBrains Mono (preços, etiquetas, dados) via Bunny Fonts — sem Google Fonts, sem rastreio. Um entalhe distintivo tipo cunho no preço (um corte de canto `clip-path`) repete-se nas etiquetas de preço, carimbos de estado e na marca do cabeçalho/rodapé, ligando todas as páginas entre si. Um segundo tema, mais minimalista, é incluído para compradores que preferem um aspeto mais simples.

**Página de destino de marketing** — Uma paleta turquesa/azul coerente com o mesmo emparelhamento Inter + JetBrains Mono, e um motivo de carimbo «MANIFEST · MBP-0001» que ecoa a própria identidade da loja, para que o site de marketing e o produto que vende pareçam uma única coisa, não dois modelos sem relação.

**Nenhum passo de build, em lado nenhum** — Cada ecrã (painel de administração, loja, páginas de marketing) é entregue com o CSS e o JavaScript já prontos. Não há nada para compilar, nenhuma dependência de Node/npm e nenhuma framework de CDN para esperar — descompacta-se e funciona.

---

## Capturas de ecrã

### Painel principal
![Painel principal](../public/images/tour/dashboard.webp)

### Produtos
![Produtos](../public/images/tour/products.webp)

### Faturas
![Faturas](../public/images/tour/invoices.webp)

### Encomendas
![Encomendas](../public/images/tour/orders.webp)

### Loja pública
![Loja](../public/images/storefront-preview.webp)

### Marketing e anúncios
![Marketing](../public/images/features/feature-marketing.webp)

### Marketplaces
![Marketplaces](../public/images/features/doc-marketplaces.webp)

### Notificações
![Notificações](../public/images/features/doc-notifications.webp)

### Utilizadores e funções
![Utilizadores](../public/images/features/feature-security.webp)

### Servidor e Segurança
![Servidor e Segurança](../public/images/tour/server-security.webp)

### Início de sessão
![Início de sessão](../public/images/screenshot-login.webp)

---

## Tecnologia

- **Laravel** 13
- **Filament** 3.3 (painel de administração)
- **PHP** 8.3+
- **MySQL** 8+
- Blade simples para a loja — nenhuma etapa de build necessária

## Instalação

Um assistente de instalação baseado na web (`/install`) trata das verificações de requisitos, configuração da base de dados, migrações, uma semente opcional de dados de demonstração, a primeira conta de administrador e dados da empresa — em 14 idiomas, e funciona quer a aplicação esteja na raiz do domínio ou em qualquer subpasta, em Apache, LiteSpeed ou nginx. Consulte `README.txt` e `public/documentation.html` para instruções completas de configuração, ou execute-o manualmente:

```bash
composer install --no-dev --optimize-autoloader
cp .env.example .env
php artisan key:generate
php artisan migrate --force
php artisan db:seed --class=DatabaseSeeder --force
php artisan storage:link
```

## Licença

Privada/comercial — consulte `LICENSE.txt`. Este repositório não é uma distribuição pública de código aberto.
