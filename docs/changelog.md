# Release Notes

## 1.1.33 — 28 October 2026

No setting was added, removed or renamed, so installing over 1.1.32 keeps your
configuration.

### Fixes

#### Home page

- **"View all" links on every product section.** Flash Sale, New Arrivals, Best Sellers and
  the "Our Products" tabs showed a "View all" link only when your store had a category named
  exactly like the demo stores ("Sale", "New Arrivals", "Best Sellers", "Featured" or "Shop
  All"). When a section has no category of its own, its "View all" now opens your store-wide
  category, sorted to match the section (newest, best selling or featured): a category named
  "Shop All", or one whose name starts with "Shop All" (such as "Shop All Store 2"), or your
  only top-level category if you have just one. A store with none of these shows no link, as
  before. A category named like the section still comes first.
  See [Homepage](usage/theme-editor.md#view-all-links-since-1133).

## 1.1.32 — 28 October 2026

No setting was added, removed or renamed, so installing over 1.1.31 keeps your
configuration. Stores whose product photos are the shape of the card (square, or 3:4 on the
Fashion style) see the same cards as before.

### Fixes

#### Product cards

- **The whole photo, never cropped.** A product photo of another shape than the card (a wide
  sofa in a square card) lost its sides. Cards on category, search and brand pages, the home
  page rows and carousels, and Recently Viewed now show the whole photo on the card's light
  ground. Square photos (or 3:4 photos on the Fashion style) fill the card as before; the
  second photo shown on hover still fills it.

#### Product page

- **No empty space under the photo.** A product with many options made a tall buying column,
  and the description tabs started only where it ended, leaving a large gap under the photo
  and another under the tabs. The tabs and videos now follow the photo directly. Phones are
  unchanged: photo, buying column, then tabs.
- **Hidden "__" custom fields.** Custom fields whose name starts with two underscores
  (`__`), as used by apps and for settings, no longer appear in the Specifications tab or
  the compare page. Name a field that way to keep it off the storefront. See
  [Product pages](usage/theme-editor.md#product-pages).
- **Long specification values stay in their column.** A long value such as a web address
  wraps inside its own cell instead of running over the next specification.
- **The reviews count matches the reviews shown.** The Reviews tab, the "N reviews" link and
  the review summary count the reviews the tab lists. BigCommerce can count reviews it does
  not show (for example reviews not approved for this storefront), which made "Reviews (6)"
  open an empty tab.
- **Recently Viewed matches Related Products.** The Recently Viewed row uses the same card
  size, columns and type as Related Products (four across from tablets up). The home page's
  Recently Viewed row is unchanged.
- **Buttons in your description respond to the pointer.** Links styled as theme buttons
  (class `button`) in a product description or warranty fill with your accent tint on hover,
  like the product page's own buttons.

#### Blog

- **"← Blog" goes back to the blog.** The link under a blog post reloaded the post instead
  of opening the blog. It now opens your blog's own address on each storefront.

#### Menu

- **Shop menu tiles in your colours.** A category tile without an image in the Shop menu
  showed an orange tint on hover with the Fashion and Food styles; it now uses your accent
  colour, and the tile name has more room underneath.

## 1.1.31 — 28 October 2026

No setting was added, removed or renamed, so installing over 1.1.30 keeps your
configuration. With the default settings every page shows the same as before. Two help
texts in **Theme Editor > Ember Theme > Homepage** are updated: the **Hero and footer pills**
note and the **Pill 2** label.

### Fixes

#### FAQ page

- **The FAQ template shows your own questions and answers.** A Web Page using the **FAQ**
  template always showed the thirteen sample questions, whatever you wrote in the page. The
  text you write in the page (**Storefront > Web Pages**) now appears under the FAQ banner,
  which takes the page's name as its heading; the sample questions, their search box,
  category filter and search-engine data are left out. A page with no text still shows the
  samples, as before. See [Page templates](usage/page-templates.md#faq).

#### Cart page

- **The returns badge follows your returns pill.** The "30-day returns" badge in the cart
  page's trust row could not be changed. It now follows **Hero and footer pills**: with
  **Built-in text** it reads "30-day returns" as before; with **Your text below** it reads
  your **Pill 2**, so one edit changes the returns promise in the hero, the footer and the
  cart; an empty **Pill 2**, or **Hidden**, removes the badge and the row closes up.

#### Home page and footer

- **Your free-shipping amount in your own pills, in the shopper's currency.** An amount
  typed into a pill ("Free shipping over $150") showed $150 to a shopper browsing in euros.
  Type `{amount}` instead ("Free shipping over {amount}"): the pill shows your **Free
  Shipping ($)** amount, converted to the shopper's currency like the top bar's default
  message. While **Free Shipping Messages** is off or the amount is 0, a pill containing
  `{amount}` is hidden. See [Hero pills](usage/theme-editor.md#hero-pills).

## 1.1.30 — 27 October 2026

No setting was added, removed or renamed, so installing over 1.1.29 keeps your
configuration; there is nothing to configure.

### Fixes

#### Home page

- **Promo banner badges stay lined up when Free Shipping Messages is off.** Under the home
  promo banner, the shipping badge has no threshold note when **Free Shipping Messages** is off
  or the amount is 0. The badges after it then slid one place, so a returns note sat beside the
  wrong title and the next badge started a line late. Where the badges stack in rows, each badge
  now starts its own row with its title and note beside its icon, whether or not the shipping
  note shows.

## 1.1.29 — 27 October 2026

One setting was added and none removed or renamed, so installing over 1.1.28 keeps your
configuration. With the default settings every page shows the same text as before. One
correction applies on upgrade: the Account created page now states your own **Free Shipping
($)** amount instead of a fixed $50, and drops that line if **Free Shipping Messages** is off
or the amount is 0.

### Fixes

#### Shipping and returns promises

- **Footer pills follow the hero pills.** The three pills in the footer ("Free shipping",
  "Secure checkout", "30-day returns") could not be changed. They now follow **Theme Editor >
  Ember Theme > Homepage > Hero and footer pills** (formerly **Hero pills**): **Built-in text**
  shows them as before, **Your text below** shows your **Pill 1** to **Pill 3** (an empty pill
  is hidden), **Hidden** removes them. See [Hero pills](usage/theme-editor.md#hero-pills).
- **Account created page: your own free-shipping amount.** The third perk said "Enjoy free
  shipping on your first order over $50" whatever your store charges. It now states your
  **Free Shipping ($)** amount, in the shopper's currency on a multi-currency store, and is left
  out when **Free Shipping Messages** is off or the amount is 0, the same rule as the top bar
  and the cart.
- **First hero slide no longer promises shipping on its own.** The theme's own first slide
  (classic look) said "... with fast shipping and hassle-free returns." When you choose **Your
  text below** or **Hidden** for the pills, that slide now reads "Browse our curated
  collection of trending products." With **Built-in text** it is unchanged. The Fashion and
  Food slides never mentioned shipping.
- **Promo banner returns note can be edited.** Under the home promo banner, the returns
  badge's note "Hassle free returns" came from the language files. **Promo returns note**
  (after **Promo Trust Badges**) replaces it with your own text; leave it empty to keep the
  built-in note.

## 1.1.28 — 27 October 2026

New settings were added and none removed or renamed, so installing over 1.1.27 keeps your
configuration. Out of the box the home page hero shows the same three pills as before;
nothing changes until you choose your own text.

### New

#### Home page

- **Hero pills: your own text, or none.** In **Theme Editor > Ember Theme > Homepage**,
  **Hero pills** controls the three short notes under the hero buttons ("Free shipping",
  "30-day returns", "Secure checkout"). Choose **Your text below** to reword them in **Pill 1**
  to **Pill 3** (leave a pill empty to hide it), or **Hidden** to remove them. If your store
  charges shipping on some or all orders, change or hide the "Free shipping" pill. The same
  choice applies when the hero is built from your Control Panel carousel slides. See
  [Hero pills](usage/theme-editor.md#hero-pills).

### Fixes

#### Blog

- **Blog cards line up.** On the blog page and in the home page blog section, a post's tag
  now sits on the top-left corner of its photo instead of above the title, so every card's
  title starts at the same height. The author and date row and "Read more" sit at the bottom
  of each card, so a short excerpt no longer leaves them floating. A post without a thumbnail
  shows a soft placeholder in your accent colour, in the same frame as a photo, instead of an
  empty box; the featured post at the top of the blog page does the same.

## 1.1.27 — 27 October 2026

No setting was added, removed or renamed, so installing over 1.1.26 keeps your configuration.
Out of the box every page looks as it did; the free-shipping messages change only if you turn
them off or set the amount to 0.

### Fixes

#### Cart and shipping

- **Free-shipping messages can be turned off everywhere.** In **Theme Editor > Ember Theme >
  Cart**, **Free Shipping Messages** (formerly **Shipping Bar**) now controls every place the
  free-shipping amount appears: the top bar's default first message, the cart sheet, the
  product page, the cart page (shipping card and the "Free ship" badge) and the "On orders
  over" note in the home promo banner. Turn it off if your store ships free on every order, or
  has no free-shipping offer. Your own first top-bar message is always shown; when it is empty
  and the messages are off, the top bar starts with its second message. An amount of 0 is
  treated the same way. See [Cart](usage/theme-editor.md#cart).

## 1.1.26 — 26 October 2026

New settings were added and none removed or renamed, so installing over 1.1.25 keeps your
configuration. Out of the box the About page looks as it did; nothing changes until you choose
your own text.

### New

#### Pages

- **About page: your own hero sentence and closing banner.** In **Theme Editor > Ember Theme >
  About page**, set **Hero sentence and closing banner** to **Your text below** to replace the
  sentence under the page heading and the closing "Ready to Shop?" banner with your own title,
  text and button. **Button link** takes a page of your store, such as `/shop-all/`; a link to
  another website opens your category list instead. Leave a field empty to hide that piece. The
  sample sentence promises shipping "everywhere", so change it if you ship to a few countries
  only. See [About](usage/page-templates.md#hero-sentence-and-closing-banner-since-1126).

### Fixes

#### Home page

- **The hero buttons no longer jump on phones while the page loads.** On screens narrower than
  480px the two hero buttons are now always stacked, so they stay put when the store's font
  arrives.

## 1.1.25 — 26 October 2026

New settings were added and none removed or renamed, so installing over 1.1.24 keeps your
configuration. Out of the box the About page looks as it did; nothing changes until you choose
your own text.

### New

#### Pages

- **About page: your own stats, value cards and story photo.** In **Theme Editor > Ember Theme >
  About page**, set **Stats** and **Values** to **Your text below** to replace the sample figures
  ("50K+ Happy Customers") and the six value cards with your own; leave a number or a title
  empty to hide that item, or choose **Hidden** to remove the section. The sample figures do not
  describe your store, so change or hide them before the page goes live. For the Our Story
  photo, upload an image in **Storefront > Image Manager** and enter its file name. Without one,
  the photo now matches your style: a living room for Home, a clothes rail for Fashion and
  pantry jars for Food. See [About](usage/page-templates.md#about).

### Fixes

#### All pages

- **The page no longer jumps while it loads on desktop.** The header logo now has its space from
  the start, so the header and the menu or search bar beside it stay put when the logo arrives.
  A page that starts shorter than the window no longer moves sideways when the scrollbar
  appears.

## 1.1.24 — 26 October 2026

No setting was added, removed or renamed, so installing over 1.1.23 keeps your configuration;
there is nothing to configure.

### Fixes

#### Pages

- **About page: the Our Story section shows the text you write for the About Us page in
  Storefront > Web Pages; with no text it keeps the built-in copy.** See
  [About](usage/page-templates.md#about).

## 1.1.23 — 26 October 2026

No setting was added, removed or renamed, so installing over 1.1.22 keeps your configuration;
there is nothing to configure.

### Fixes

#### Pages

- **About page team photos show each person's whole head, with room above it.** Before, on desktop
  and tablet the photos were cut to a short, wide strip, so heads touched the top edge and hair was
  cut off. On phones the photos stay square.

## 1.1.22 — 26 October 2026

No setting was added, removed or renamed, so installing over 1.1.21 keeps your configuration;
there is nothing to configure.

### Fixes

#### Home page

- **Meet the Makers shows every brand image whole, photos and logos alike (Food style):** in 1.1.21
  a brand image saved as PNG, SVG, WebP or GIF was enlarged to fill its tile, so a brand photograph
  saved as PNG was still cut at the top and bottom. Now every brand image, whatever its format, sits
  whole and centred in its tile with the same even margin. If a logo has a wide empty margin of its
  own and looks small, crop that margin from the image and upload it again in
  **Products > Brands**.

## 1.1.21 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.20 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Product photos in the cart sit in one square frame:** the small product photos in the cart, the
  cart drawer, the added-to-cart window and your account's orders and returns are all the same
  square again, so every line looks alike. The whole photo is shown, centred in the square; a wide
  or tall photo has an even margin on both sides (in 1.1.20 each photo's frame took its own shape).
  Square photos fill the square as before, and nothing on the page moves while the photos load.

#### Home page

- **Meet the Makers shows a photo whole (Food style):** a maker shown with a photograph instead of a
  logo is no longer cut at the top and bottom of its tile; it sits whole and centred with an even
  margin. Transparent logos (PNG, SVG, WebP) keep their size.
- **A category without an image looks light (Food and Fashion styles):** a category card with no
  image no longer has a dark band over its placeholder. The name is shown in your heading colour on
  the light placeholder (light text in dark mode). This applies on the home page and the All
  Categories page; cards with images are unchanged.

## 1.1.20 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.19 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Product photos in the cart keep their own shape:** the small product photos in the cart, the
  cart drawer, the added-to-cart window and your account's orders and returns now take the shape
  of the photo instead of a fixed tile. A wide photo shows whole as a wide thumbnail, with no empty
  space above and below it (in 1.1.19 it sat as a thin strip in a large empty tile). Square photos
  fill a square, and only a photo taller than the usual tile is shown slightly narrower. Nothing
  on the page moves while the photos load.

## 1.1.19 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.18 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Whole product photo in the cart:** the small product photos in the cart, the cart drawer and
  your account's orders and returns show the whole product instead of cutting off the ends of a
  wide photo.

#### Home page

- **Shop by Category with only a few categories:** with fewer categories than fill a row (one to
  three, for example), the cards sit in the middle of the row at their usual size, right above
  "View all categories", instead of at the left edge with the link far from them. Stores with a
  full row look the same as before.
- **Meet the Makers with only a few brands (Food layout):** one to three brands show as
  normal-size logo tiles in the middle of the row instead of one tile stretched across the whole
  page.

#### Header

- **Categories menu without subcategories:** when your categories have no subcategories and no
  category images, the Categories menu opens as a neat list of your categories instead of a large
  panel with an empty area beside it. In a larger menu, a category without an image now shows its
  name and an "All" link where its image would be, instead of a blank area.

## 1.1.18 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.17 keeps your configuration;
there is nothing to configure.

### Fixes

#### Header

- **Header stays still in dark mode:** the header no longer grows a moment after the page opens
  in dark mode when a dark logo is set. The dark logo now takes the place your regular logo has
  reserved, at the same size, and the regular logo is fetched first so that place is ready sooner.

#### Cart

- **Product names hold their line:** product names in the cart no longer nudge the page by a pixel
  when the font loads.

#### Product page

- **Options are there from the start:** a product's options (size, colour and so on) show as soon
  as the page appears, instead of a moment later and pushing Add to Cart down. The estimated
  delivery line keeps its height while the date is worked out.

## 1.1.17 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.16 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Order summary stays still:** the cart's order summary no longer moves down a moment after
  the page opens: the Shipping row keeps its height while free shipping is checked. Before a
  shipping cost is known the row reads "Calculated at checkout" (or FREE once the cart reaches
  your free-shipping amount), with "Estimate shipping to your address" on a quiet line under it.

## 1.1.16 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.15 keeps your configuration;
there is nothing to configure. One default changed: the Home style's checkout button now hovers
in the theme's burnt orange (#B84600) instead of the bright #FF6A00. To keep the previous
colour, set the optimized checkout primary button hover colour back to #FF6A00 in Theme Editor.

### Fixes

#### Home page

- **Promo banner headline reads in two balanced lines:** "Our" no longer sits alone above
  "Best Sellers"; the headline is now "Best Sellers / At Special Prices", in every language the
  theme ships.

#### Product listings

- **Category banners are lighter:** the shade behind the title on a category's banner photo no
  longer covers half the photo in solid black. It sits only behind the text, in a warm tone,
  and fades out well before the far edge, so more of the photo shows. The breadcrumbs, title and
  description stay as readable as before (WCAG AA on every banner photo of the demo stores).
- **Brand page header:** the brand's logo shows in a larger tile, so its name is readable, and
  the header sits closer to the breadcrumbs, as on the other listing pages.

#### Compare

- **No broken image in the compare bar:** if a product's photo is removed after a shopper
  added it to the compare bar, the bar shows your store's default product image instead of a
  broken-image icon. The bar also picks up a product's current photo whenever that product is
  shown on the page.

#### Cart

- **Gift wrapping on a cart line:** once a shopper chooses gift wrapping, the quantity, edit,
  gift and delete buttons stay on one row, and the chosen wrap (name, price, Change, remove)
  shows on its own line under them, followed by the gift message. Works on phones too.

#### Checkout

- **Continue button:** clicking Continue no longer leaves a heavy orange glow around it.
  Hovering shows a light shadow, and the focus ring appears only for shoppers using the
  keyboard.

#### Pages

- **About page "Ready to Shop?" block** is narrower and centred, with the same space under it
  as between the other sections, instead of a full-width orange band followed by a large gap
  before the footer.

#### Prices

- **Discount badges use the shopper's currency:** the "-N%" badges in quick search, the product
  comparison and the sticky Add to Cart bar now read the currency the page is shown in, not the
  first currency listed in the header's currency switcher.

## 1.1.15 — 25 October 2026

No setting was added, removed or renamed, so installing over 1.1.14 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Order summary no longer shifts when the cart page loads:** shoppers whose cart was in a
  currency other than your default one saw the Gift Certificate row disappear about half a
  second after the page appeared, and the Check out button jumped up. The row now stays put in
  every currency, and a gift certificate can be applied in a cart of the certificate's own
  currency, from that row or from the promo code field.

## 1.1.14 — 24 October 2026

No setting was added, removed or renamed, so installing over 1.1.13 keeps your configuration;
there is nothing to configure.

### Fixes

#### Header

- **Store name shows in full:** a store that has no logo image shows its name in the header. A
  long name now wraps onto two lines, a little smaller if needed, instead of being cut off with
  "…". Short names and logo images look the same as before.

## 1.1.13 — 24 October 2026

Adds one setting; nothing was removed or renamed, so installing over 1.1.12 keeps your
configuration. The new **Show Apple Pay** setting starts off, so your payment icons look the
same until you turn it on. The gift wrapping dialog's "choose a gift wrap" text is shorter in
every language.

### New

#### Payment icons

- **Apple Pay icon:** turn on **Theme Editor → Header and footer → Payment icons → Show Apple
  Pay** to add an Apple Pay icon next to your other payment icons in the footer, the cart, the
  product page and the cart drawer. It is off by default.

### Fixes

#### Cart

- **Gift wrap choice fits on phones:** the "Choose gift wrap" text in the gift wrapping dialog
  fits in the box on phones in every language, instead of being cut off.

#### Home page

- **Cleaner hero slide change:** when the hero slides change, only the pictures crossfade; the
  old and new headings no longer overlap while the slide changes.

#### Category and brand pages

- **No product lookups on listing pages:** category and brand pages no longer ask the store for
  product data just to count products. A category's product count comes from the page itself;
  a brand's count shows when all of its products fit on one page. Brand logos in the Brands
  menu load when the menu is first opened instead of on every page.

#### Breadcrumbs

- **Breadcrumbs on phones:** the breadcrumb trail now shows on phones on product, category,
  brand, brands and web pages, on one line; long names in the middle shorten with an ellipsis
  so the current page stays readable. **Hide breadcrumbs** still removes it.

## 1.1.12 — 23 October 2026

No setting was added, removed or renamed, so installing over 1.1.11 keeps your configuration;
there is nothing to configure.

### Fixes

#### Dialogs

- **Close button lines up with the title:** the close button in every dialog (gift wrapping,
  write a review, and every other one) sits on the same line as the dialog title instead of
  slightly below it, and stays beside the first line when a long title wraps.

## 1.1.11 — 23 October 2026

No setting was added, removed or renamed, so installing over 1.1.10 keeps your configuration;
there is nothing to configure.

### Fixes

#### Blog

- **Blog card photos:** blog cards on the home page ("Latest from Our Blog") and the blog page
  show each post's photo in a 4:3 frame instead of a thin strip, so portrait photos are no
  longer cut down to a band. On the Food style's home page, where the blog cards sit side by
  side on wider screens, the photo still fills its column.

#### Header

- **Switching currency with items in the cart:** when a shopper picks another currency while
  their cart has items, the cart and the page change to that currency together in one step,
  and the switch no longer risks losing the cart.

## 1.1.10 — 23 October 2026

No setting was added, removed or renamed, so installing over 1.1.9 keeps your configuration;
there is nothing to configure.

### Fixes

#### Cart

- **Gift Certificate field in other currencies:** the Gift Certificate field stays available
  when a shopper views prices in another currency but their cart is still in the store's
  default currency.

## 1.1.9 — 23 October 2026

No setting was added, removed or renamed, so installing over 1.1.8 keeps your configuration;
there is nothing to configure. The promo code field in the cart now reads "Promo code", and the
new gift certificate field reads "Certificate code" (stores that allow several promo codes per
order).

### Fixes

#### Cart

- **Gift Certificate row:** on stores that allow several promo codes per order (BigCommerce's
  newer cart summary), the cart summary has its own Gift Certificate row, next to the promo code
  row. Shoppers select **Add** to open a code field and **Apply** to redeem it, the same way the
  promo code works. The row is hidden when the shopper is browsing in a currency where gift
  certificates can't be used. Stores on the classic cart summary keep the gift certificate field
  as it was.
- **Promo code field:** the field is now labelled "Promo code". It still accepts a gift
  certificate code.
- **Currency after switching:** after a shopper switches currency, the cart now uses the
  currency they picked instead of the one they were in before.
- **Quantity buttons:** tapping the − and + buttons on the product page, quick view, cart and
  cart drawer no longer flashes the browser's blue highlight; the button shows a pressed state in
  your theme's accent colour. Keyboard users still see the focus outline.

#### Header

- **Search bar corners:** the header search bar follows your theme's corner radius instead of
  always being fully rounded; the Fashion style keeps square corners. The search box on phones
  follows the same setting.

## 1.1.8 — 22 October 2026

Adds one setting; nothing was removed or renamed, so installing over 1.1.7 keeps your
configuration. The new **Category header with an image** setting starts on Banner (the Fashion
style starts on Split). The gift card preview now labels its names "To" and "From".

### New

#### Category pages

- **Category header banner:** when a category has an image, the photo now sits behind the
  breadcrumb and title as a banner, with a shade that keeps the title easy to read. Choose the
  look in **Theme Editor → Global → Products → Category header with an image**: **Banner**
  (photo behind the title, the default) or **Split** (title beside the whole photo, as before).
  The Fashion style uses Split. See [Category pages](usage/theme-editor.md#category-pages).

### Fixes

#### Gift certificates

- **On-brand gift card preview:** the gift card preview on the purchase and balance pages uses
  your theme's accent colours. It shows the amount the shopper picked, in the currency they are
  shopping in, instead of $0, and the To and From names update as they type.

#### Mega menu

- **Opens smoothly:** the category photo in a mega menu fades in when it loads instead of
  flashing in at full brightness, and moving between menu items crossfades the panels.

#### Header

- **Cleaner search button:** the search button closes off the end of the header search box
  neatly, without a double outline.

#### Cart

- **Edit options window fits its content:** the window for changing a cart item's options is
  sized to its content instead of stretching across the page; option buttons match the product
  page and Save spans the full width.

## 1.1.7 — 22 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.6 keeps your configuration; there is nothing to configure.

### Fixes

#### Mega menu

- **Page dims again under an open menu:** when a mega menu panel is open, the rest of the page
  is dimmed again, as intended. On live stores the dimming had stopped showing.

#### Filters

- **One scrollbar on category, brand and search pages:** the filter sidebar now scrolls with
  the page instead of inside its own box, so a long filter list no longer shows a second
  scrollbar. It still stays in view while you scroll when it is short enough to fit under the
  header.

#### Product page

- **Quantity stepper:** the quantity is now a box with − and + buttons, and shoppers can also
  type a quantity. There is no longer a limit of 20; the product's own minimum and maximum
  purchase quantities still apply. Quick view uses the same stepper.
- **Buttons fill on hover:** the wishlist, compare and Buy Now buttons and the quantity − and +
  buttons fill with colour when you point at them, and Add to Cart turns a shade darker.
- **Tabs no longer jump:** switching between Description, Specifications and Reviews keeps the
  tabs where they are instead of jumping the page.
- **Payment, trust and share block:** the payment icons, trust badges and share buttons line up
  on one left edge with even spacing, and the Print share button has a border like the others.
- **Specifications:** each value now sits right beside its label instead of at the far edge of
  the column.

#### Cart

- **Cart page quantity:** the quantity stepper on the cart page has the same height and corner
  shape as the edit and remove buttons next to it.
- **Compact cart sheet:** the cart sheet that slides in after Add to Cart is more compact, so a
  laptop screen shows three or more products at once; the promo code link stays visible.

#### Food style: home page offers

- **Smoother offer tile shade:** the darkening behind the text on the Food home page offer tiles
  fades out smoothly instead of ending in a visible edge.

## 1.1.6 — 22 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.5 keeps your configuration; there is nothing to configure.

### Fixes

#### Food style: home page offers

- **Lighter offer tiles:** the two offer tiles on the Food home page are brighter. The
  darkening now sits only behind the text (at the bottom of the tile, and on the left of the
  deal tile on tablets and desktops) instead of over the whole photo, and the theme's own
  photos are slightly brightened. A banner image you upload yourself is shown as uploaded.

#### Mobile menu

- **Open currency and language lists:** when you open the currency or language list in the
  mobile menu, its arrow turns up and the list reads as one group under it. The selected
  currency is shown in the accent colour with a smaller check.

#### Filters

- **No underline on tapped filter headings:** on phones and tablets, a filter heading you tap
  (such as Rating or Price) no longer stays underlined.

## 1.1.5 — 21 October 2026

Installing over 1.1.4 keeps your configuration: no setting was removed or renamed, and no
storefront text changed. The Food variation has new default colours (below). A store that
already uses Food keeps the colours it has saved; it gets the new palette only when the Food
variation is applied again with its original (default) settings, or when you set the colours
yourself in Theme Styles.

### Changes

#### Food style: olive and cream

- **New default palette:** the Food variation now uses deep olive (#4F5B2A) for buttons, links
  and the navigation band, on a fresh cream page (#FBF8F1), with tomato red (#C2401C) for sale
  badges and the flash-sale countdown. In dark mode the accent is a sage green. Before, Food
  was terracotta on beige and looked close to the Fashion style. Three new Food colour defaults
  are set for sale and warning colours; nothing else needs configuring.

### Fixes

#### Category pages

- **Compact category header with the whole photo:** the category title and description sit on
  the left and the category image on the right, at a fixed height (240px on desktop, 200px on
  tablets) and at its own shape, so nothing is cut off. On phones the image sits under the
  title. A category without an image or description shows only what it has, without an empty
  panel. The title size now matches the brand pages.

#### Faster images

- **Sized images instead of full-size originals:** blog cards on the home page, the blog page
  and the blog post header, compare-table thumbnails and pattern swatch previews now load an
  image sized for where it is shown, instead of the full original upload.
- **Responsive theme images:** the theme's own promo banners, Lookbook scenes and Lookbook room
  tiles load a size that fits the screen (400, 800 or 1200px wide, WebP where the browser
  supports it). Images you upload yourself are unchanged.

#### Theme package

- **Marketplace screenshots:** the Food screenshots in the theme package show the new palette.

## 1.1.4 — 20 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.3 keeps your configuration; there is nothing to configure.

### Fixes

#### Home page hero (Fashion and Food styles)

- **More of the hero photo on wide screens:** on screens wider than about 1320px, the home page
  hero in the Fashion and Food styles grows taller with the width, up to the height of the
  window below the header, instead of staying 620px tall and cutting off the top and bottom of
  the photo. In the Fashion style, when the window is too short to show the whole photo, more
  is cut from the bottom than the top, so heads and bag handles stay in view. Phones, tablets
  and narrower desktops look as before.
- **Your own carousel images:** when the hero shows your Control Panel carousel, the shape of
  the first slide's image sets how tall the hero grows; a very wide banner image keeps the
  620px height.
- **Fashion: copy centred:** from 801px wide, the hero headline and buttons in the Fashion
  style sit in the middle of the photo's height instead of near the top.
- **With a banner above:** when a marketing banner or a widget sits above the hero, the hero
  keeps its 620px height.

The Home style's hero is unchanged.

## 1.1.3 — 20 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.2 keeps your configuration; there is nothing to configure.

### Fixes

#### Category pages

- **Sharper category banner:** from 600px wide, the category banner puts the title and
  description on a text panel and shows the category image beside it, in a box 42% of the
  banner's width and as tall as the banner (at least 260px, 320px on wide screens), instead of
  a photo stretched behind the text with most of it cut off. The image is drawn close to its
  own size, so it stays sharp; it is still cropped to fill its box, so a landscape image
  (around 3:2) with the subject in the middle works best. Phones keep the photo behind the
  text.
- **Same category tiles everywhere:** the category tiles on the All Categories page now look
  the same as the home page tiles in each style. In the Fashion and Food styles that is the
  dark band with the white name on every photo; before, light photos on All Categories switched
  to a pale band with dark text.
- **Readable tile arrow:** the arrow on category tiles keeps the name's colour on hover, so it
  stays easy to see in the Home and Fashion styles (the Food style has no arrow).
- **Filters:** the Clear button in the filter sidebar appears only once a filter is set. On
  stores without product filtering, the price-only sidebar is more compact, and its Min field
  lines up with the Update button.

#### Fashion style

- **New hero image:** the second home page hero slide in the Fashion style has a new photo.

#### Theme package

- **Image provenance:** `assets/PROVENANCE.md` records the new hero image.

## 1.1.2 — 20 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.1 keeps your configuration; there is nothing to configure.

### Fixes

#### Fashion style

- **Option labels centred:** on the product page in the Fashion style, size and colour option
  labels sit in the middle of their boxes instead of near the top.

#### Theme package

- **Image provenance:** `assets/PROVENANCE.md` now also records the extra product photos added
  to the demo stores.

## 1.1.1 — 17 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.1.0 keeps your configuration; there is nothing to configure.

### Fixes

#### Readability

- **12px minimum text size:** every text in the theme is now at least 12px at every screen
  width, including the "Required" note on account forms, small labels, badges, the header cart
  and wish list counts, and printed invoices. The cart's trust tiles keep "Secure checkout" on
  one line.

#### Phones and tablets

- **Larger tap areas:** on touch screens up to 1024px wide, these controls now have 44px tap
  areas while looking the same: the wish list remove button and wish list actions, product
  colour swatches (including "None"), Lookbook markers, blog tags and categories, address Edit
  and Delete links, account menu and order filters, search result and FAQ tabs, the header logo
  on tablets and the Food hero arrows. Layouts with a mouse are unchanged.

#### Footer

- **X icon for a social link named "X":** a social media link named "x" now shows the X mark in
  the footer, as one named "twitter" already did, instead of a generic globe.

## 1.1.0 — 17 October 2026

Feature release. Installing over 1.0.7 keeps your configuration: no setting was removed or
renamed. Three settings are new, under Theme Styles > Products > Featured promotions, and start
with the values below. Two new storefront texts ship translated in every language file.

| New setting | Default |
|---|---|
| Show featured promotions (`show_featured_promotions`) | On |
| Promotion background (`yen-offer-bg-color`) | Home #FFF7ED, Fashion #F7F3EC, Food #FBEFE6 |
| Promotion text (`yen-offer-text-color`) | Home #B84600, Fashion #7A5D33, Food #8C3B26 |

### New features

#### Featured Promotions

- **Promotion callouts on products:** when you feature an automatic promotion and give it a
  callout, the callout shows under the price on product cards (category, brand, search, home
  sections, related products, quick search), on the product page and in quick view. Cards show
  the top promotion and "+N more offers"; the product page and quick view list every one. Turn
  it off, or change its colours, in Theme Styles > Products > Featured promotions. Dark mode
  builds the callout colours from your Dark Mode Colors.
- **BigCommerce rollout:** BigCommerce is enabling featured promotion data store by store.
  Until it is on for your store, no callouts appear, and nothing else changes.

#### Backorders

- **Backorders on the product page and in quick view:** a product that can be backordered keeps
  Add to Cart when nothing is on hand (it is no longer labelled Sold Out), shows the
  availability prompt, how many units will be backordered and the product's backorder message
  (or your store's default message), and, for pick-list options, each option's own lines. A
  quantity above what can be sold disables Add to Cart with "The maximum purchasable quantity
  is N", also per pick-list option. The "Get it by" delivery estimate is withdrawn while any
  unit is backordered.
- **Backorders in the cart and orders:** cart lines, in the cart page and the cart panel, show
  how many units are ready to ship, how many will be backordered and the backorder message,
  with a group per pick-list option, and the cart summary adds your shipping expectation when
  the cart holds a backordered item. Order details in My Account show the same lines under each
  product and the shipping expectation under the shipping address. What shows follows your
  Settings > Inventory choices. Backorder quantities appear only when Settings > Inventory >
  Stock level display is not "Don't show": BigCommerce sends no backorder figures while stock
  levels are hidden.

### Fixes

#### Product page

- **Sold-out variant after an in-stock one:** choosing a sold-out variant after an in-stock one
  now disables Add to Cart and shows Sold Out; the earlier variant's stock figure no longer
  carries over. A quick view opened over a product page reads its own product's stock, not the
  page product's.

#### Shipping

- **No free-shipping promise next to a fixed shipping cost:** a product with its own fixed
  shipping cost no longer shows the free-shipping bar on the product page; the line by Add to
  Cart states the cost instead. In the cart page and the cart panel, the free-shipping progress
  and "FREE" are left out when every product in the cart has a fixed shipping cost.

#### Tablets

- **Larger tap areas on touch tablets:** on tablets (768 to 1024px wide, touch screens), footer
  links, social icons, pagination, brand letters, grid/list toggles, the top-bar currency and
  light/dark buttons, product option chips and Lookbook markers have 44px tap areas. Layouts
  with a mouse are unchanged; the footer gets a little taller on tablets.

#### Theme package

- **Image provenance:** the theme package includes `assets/PROVENANCE.md`, which records how
  each bundled and demo image was made and its licence terms.

## 1.0.7 — 16 October 2026

Maintenance release. No setting or storefront text was added, removed or renamed, so installing
over 1.0.6 keeps your configuration; there is nothing to configure.

### Fixes

#### Account

- **Wishlist Add to Cart readable in dark mode:** on a wishlist page in dark mode, the Add to
  Cart button label was dark on the dark card and almost invisible, and in light mode its
  outline was very faint. The label, the outline and the hover fill now follow the colour mode.
  The Pre-order button and the stock note below it are easier to read too.

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
