# Release Notes

## 1.0.7 — 16 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.0.6 keeps your configuration; there is nothing to configure.

### Fixes

#### Account

- **Wishlist Add to Cart readable in dark mode:** on a wishlist page in dark mode, the Add to
  Cart button label was dark on the dark card and almost invisible. The label, the outline and
  the hover fill now follow the colour mode. The Pre-order button and the stock note below it
  are easier to read too.

## 1.0.6 — 16 October 2026

Maintenance release. No setting was added, removed or renamed, so installing over 1.0.5 keeps
your configuration. Two new storefront texts, the promo code links in the cart panel below,
ship translated in every language file; there is nothing to configure.

### Fixes

#### Account

- **Wishlist cards show the product again:** on a wishlist page, the product photo no longer
  covers the card, so the name, the price and the Add to Cart button are visible and can be
  tapped.
- **Clearer "Required" labels:** the "Required" note next to form fields is 12px at every
  screen width, the same as on phones.

#### Currency

- **Switching currency without a cart:** choosing another currency before anything is in the
  cart now switches the store currency straight away, with no error in the browser console.
  With items in the cart, the cart changes to the new currency as before.
- **Fashion currency button:** in the Fashion style, the currency button in the top bar is as
  large and easy to tap as in the Home style.

#### Cart

- **Promo codes in the cart panel:** the cart panel now shows a link, "Have a promo code? Apply
  it in your cart" (or "promo code or gift card" when gift certificates are on), that opens the
  cart page, instead of a field that could not be typed in.
- **Easier quantity buttons:** the - and + buttons in the cart panel have a larger tap area on
  phones and tablets, and with a mouse on small laptops; they look the same.
- **Remove confirmation in the theme style:** removing an item from the cart panel asks for
  confirmation in the theme's own dialog, the same one the cart page uses, instead of the
  browser's plain pop-up. Pressing Escape closes the dialog and leaves the cart panel open.

#### Food style

- **Readable reviews in dark mode:** in the Food style in dark mode, the review date and the
  "Verified" badge on home page testimonials have stronger contrast.

#### Pages

- **Newsletter confirmation pages:** the pages shown after subscribing, unsubscribing or
  creating an account no longer show a white band above the content panel.
- **Sale link:** when no promo banner link is set, the home page promo button opens /sale/
  directly, without a redirect.

## 1.0.5 — 15 October 2026

Maintenance release. No setting was added, removed or renamed, so installing over 1.0.4 keeps
your configuration. One new storefront text, the "Added to cart" heading below, ships
translated in every language file; there is nothing to configure.

### Fixes

#### Phones

- **Newsletter sign-up in one row:** in the footer and the home page newsletter band, the email
  field and its subscribe button now sit in a single row, with an arrow button inside the end
  of the field, instead of a field stacked over a full-width button. Tablets and desktops look
  as before.
- **Sign in first in the mobile menu:** at the bottom of the menu drawer, Sign in is the filled
  main button and Register (Log out when signed in) the outlined one, and the drawer no longer
  ends in a band of empty space.
- **Closer hero slide dots:** the slide dots on the home page hero are larger and closer
  together, each still easy to tap, and the pause button is easier to hit. Tablets and desktops
  look as before.
- **Calmer tap feedback:** tapping a link or button no longer flashes a grey square over
  rounded chips and tiles. Category chips, category tiles and hero buttons show a brief colour
  change when pressed instead.

#### Cart

- **"Added to cart" after adding:** the cart panel that opens after Add to Cart is headed
  "Added to cart" with a check mark, so shoppers see at once that the item went in. Opened from
  the cart icon in the header it still reads "Your Cart".

#### Product images

- **Image backgrounds blend in light mode:** product photos on cards, in Quick View, on the
  product page and in the cart sit on a soft background matched to each style (Home, Fashion,
  Food), so photos shot on an off-white studio background no longer show as a separate pale
  box. Dark mode, banners, lookbook, category and brand images are unchanged.

## 1.0.4 — 15 October 2026

Maintenance release. No setting was added, removed or renamed, so installing over 1.0.3 keeps
your configuration.

### Fixes

#### Header

- **The logo follows its size setting:** a "Logo image size" other than the default 250x100 in
  the Theme Editor can now make the header logo larger, up to 80px tall on tablets and
  desktops, and the header row grows with it. Before, the logo was capped at 56px (44px in
  Fashion), so a larger size could only shrink it. The default size looks as before, and phones
  keep their 40px logo.

#### Product cards

- Keyboard users tab through a product card from top to bottom: the wish list, Quick View and
  compare buttons drawn on the product image come before the product name and the add to cart
  button. Nothing moves on screen.

#### Category pages

- A widget placed in the region below the product list (`category_below_content`) lines up
  with the products column beside the filter sidebar, spans the page where the filters are in
  the drawer, and no longer runs under the footer.

#### Accessibility & touch

- On touch screens, radio button labels in forms get a 44px tap row like the checkboxes, and
  the checkbox and radio boxes line up with the first line of their label.

## 1.0.3 — 15 October 2026

Maintenance release. No setting was added, removed or renamed, so installing over 1.0.2 keeps
your configuration.

### New

- **Two home page widget regions** for Page Builder: `home_above_products`, directly above the
  first product feed (above the product tabs in Home and Fashion, above the New Arrivals shelf
  in Food), and `home_above_footer`, at the end of the page above the footer.
- **Quick View follows its setting:** "Show quickview button on product cards" now removes the
  button everywhere when off. When on, the button also shows on touch tablets (768px and
  wider), including the narrow cards of the home tabs and Food shelves.
- **Share buttons follow the control panel:** the product page shows the social sharing buttons
  you pick in the control panel, including Print and Facebook Like.

### Fixes

#### Product page

- Adding to a wish list from the product page saves the item again; before, the request went
  out empty and nothing was added.
- The wish list menu is no longer cut off on screens 860-1090px wide.
- No "Get it by" delivery date on pre-order products.
- A fixed shipping cost is shown in the shopper's currency.
- Products with a price range show no strike-through price until a variant is chosen.
- The free-shipping progress bar no longer counts the item just added twice.
- A product with one image shows no thumbnail strip.
- The review form fields line up, and the confirmation message scrolls into view after sending.

#### Cart

- One "Promo code or gift card" box tries the code as a coupon, then as a gift certificate. In
  a currency other than your default it reads "Promo code", because BigCommerce only accepts
  gift certificates in the default currency. Applied gift certificates still list with Remove.
- Order Summary: discounts on their own row, the shipping amount on one line, no "FREE" when
  every shipping option costs money, and a visible arrow in dark mode.
- The cart lines up with the page title.
- Escape closes the cart drawer and returns focus to the cart button.
- Product Set widget dots on the cart page no longer show over the sticky header.
- The free-shipping card matches the warm card colour in Food dark mode.
- The gift certificate Remove link no longer touches its amount.

#### Search & filters

- The filters sidebar is hidden on the News & Information search tab.
- Brand pages: the price filter chip is formatted as currency, filtering down to no products
  shows the empty-results message, and stores without faceted search keep the Filters button
  and Shop by Brand drawer.
- The /brands/ page uses the brand image size setting.

#### Home & footer

- Hero slides: the old caption fades out before the new one appears.
- Several marketing banners in one location no longer print a stray comma.
- Promotion notices on the home page stay inside the page width.
- The footer newsletter form shows on every page, uses your control panel newsletter summary
  when one is set, and tells shoppers who are already subscribed.
- Home blog excerpts end on a whole word with an ellipsis.
- Brand initial tiles are readable in dark mode.

#### Account

- The Create Account tab is hidden when account creation is turned off.
- Account pages: heading spacing on tablets and desktops, and the Email field styled like the
  other fields.

#### Checkout and other pages

- Checkout, order confirmation, maintenance and hibernation pages keep the logo readable on
  dark headers: the dark-mode logo when set, otherwise a light plate behind the logo.
- Web page content follows the body font size setting.
- Products without an image show a sharp SVG placeholder.

#### Accessibility & touch

- On touch screens, buttons and controls get a 44x44px tap area: main buttons, cart quantity,
  edit and remove, the sticky add to cart, home tabs, Lookbook card buttons, the filter drawer
  close button, card icons and share buttons. Mouse use on desktop is unchanged.
- Better contrast for testimonial initials, Lookbook hotspot numbers and the gift certificate
  icon in dark mode.
- The cart icon announces the item count with the right plural form in every language.
- Compare page links and Product Set dots meet the minimum target size.
- Cart item options are read as label and value pairs by screen readers.

#### Mobile/tablet layout

- Lookbook "Choose options" buttons are no longer clipped at 761-820px in Fashion.
- Long brand names on product cards wrap to two lines instead of being cut off; card rows stay
  aligned.
- Compare page: a Sold Out label for sold-out products and star rows aligned across columns.
- The product page share row wraps on small phones instead of being cut off.
- Food shelves at 320px keep the stars and review count on one line.
- The quick search panel on tablets lines up with the search field.
- Currency menu title and Quick View brand text are slightly larger.

### Other

- The Outfit font is only loaded by the Home layout, so Fashion and Food pages load less.
- New storefront texts are translated into all 20 languages; some are machine translations.
- Marketplace descriptions corrected for the Home font and the Fashion header.

## 1.0.2 — 14 October 2026

- Theme renamed from Yen to Ember. Settings, layouts and features are unchanged.

## 1.0.1 — 14 October 2026

Maintenance release. No settings change; installing over 1.0.0 keeps your configuration.

### Fixes

- **Create account:** every custom sign-up field you add in the control panel now shows.
  Fields whose name contained words such as "Birthday" or "Pay by PO" were hidden and lost
  their required flag.
- **Account menu:** Messages and Recently Viewed are back in the account sidebar and on the
  dashboard.
- **Account dashboard:** order, wish list and return counts are no longer capped at the number
  of items previewed; a long list shows "N+". The Addresses count, which BigCommerce does not
  provide on this page, was removed.
- **Account settings:** Chrome no longer fills the saved password into New Password, which
  blocked saving a name or email change. The password fields sit in their own "Change
  password" group with a hint, and form fields carry the right autocomplete values.
- **Maintenance and hibernation pages:** the browser tab shows the page heading instead of an
  empty title, and an empty favicon or logo is no longer printed.
- **Newsletter confirmation pages:** buttons keep readable contrast on hover and focus in all
  three variations, light and dark; the breadcrumb names the current page. The default
  newsletter and home promo banner text no longer promises a fixed discount ("up to 30% off",
  "Up to 50% OFF") in any language.

### Other

- Security patches to build tools. No storefront change.

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

- Home hero shows your Storefront → Carousel slides when you add them, in the theme's own
  hero design; without slides it shows the theme's three built-in slides
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
