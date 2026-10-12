# Release Notes

## 1.0.0 — Initial release

Yen Theme for BigCommerce, built on Cornerstone 6.19.0.

### Variations

Three, with the same features. Each has its own layout preset (Theme Editor → Yen Theme
→ Layout Preset) as well as its own colours and type.

- **Home** — Classic layout, the theme's own defaults
- **Fashion** — Editorial layout: centred logo, full-bleed hero, display serif, brass
  accent, opens in dark mode
- **Food** — Market layout: search-first header, round category tags, five-across home
  grids, herb green, its own photographs and copy

### Shopping experience

- Dark/light mode toggle, with both modes designed rather than inverted
- Mega navigation with featured images and multi-column layouts
- Product cards with quick view, wishlist, compare and hover detail
- Grid and list view on category, brand and search pages
- Faceted search with a sidebar on desktop and a drawer on mobile
- Cart page with a summary sidebar, shipping estimator and gift certificates

### The Lookbook

Shoppable images: place hotspots on a photograph as percentage coordinates and map each one
to a product ID. 41 settings, and a page template of its own.

### Custom page templates

Four, each chosen from the template dropdown when creating a web page: **Lookbook**,
**About**, **FAQ** and **Track Order**. All four render their own content — the page body
you type is not what appears. See [The other page templates](usage/page-templates.md) for
what that means in practice.

### Homepage

Hero banner, trust badges, brand showcase, flash sale, reviews, press mentions and
newsletter, each with its own on/off switch in the Theme Editor.

### Under the hood

- Full Page Builder and Theme Editor integration — 380 settings across 9 sections
- Lazy loading with low-quality image placeholders, so images resolve in rather than jump
- Responsive from phone to desktop, with the desktop layout starting at 1261px
- Accessibility: ARIA attributes throughout, focus trapping in overlays, keyboard
  navigation, named landmarks, and a single main landmark per page
- 20 storefront locales covering 13 distinct translations

### Phones and tablets

- Every page reworked for phones, tablets and phone landscape, in both colour modes, and
  readable at up to 200% text size
- Add to Cart opens the cart as a sheet over the page instead of leaving the product
- A per-slide **Hero Focus (phones & tablets)** setting keeps each hero photograph's
  subject in view when the picture is cropped — see
  [Hero focus](usage/theme-editor.md#hero-focus-on-phones-and-tablets)
- One button system per layout preset, with the hover and pressed shades mixed from the
  **Button** colour

### Cart

- The cart page, the cart sheet and the product page say how much more qualifies for free
  shipping, in the shopper's currency
- The cart page's cross-sell row leaves out products already in the cart
- A promotion that splits a discounted unit onto its own line shows as one product, and
  minimum and maximum purchase quantities count across both lines

### Prices hidden from guests

When the store hides prices from guests, no price reaches the page: not on product cards,
bulk pricing tables, the product page's fixed shipping cost, the free-shipping bar, or the
structured data search engines read. See
[Prices hidden from guests](usage/theme-editor.md#prices-hidden-from-guests) for what that
means for Google rich results.

### Upgrading from a pre-release build

- **Fonts:** pick your body and heading fonts again so every weight loads — see
  [Typography](usage/theme-editor.md#typography).
- **Primary button colour:** `#1B1D21`, `#333333` and `#000000` in the Cornerstone primary
  button controls read as "not set" — see
  [Primary button colour](usage/theme-editor.md#primary-button-colour).

### What the theme does not do

- **No external services and no API keys.** Everything rendered comes from your own catalog
  and settings.
- **No order-lookup form on Track Order.** BigCommerce provides no storefront endpoint a
  theme can query for a guest's order, so the page offers what does work: order history for
  signed-in shoppers, and the emailed tracking link for guests.
