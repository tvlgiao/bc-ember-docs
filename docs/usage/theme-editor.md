# The Theme Editor, section by section

The editor is organised into nine sections. One of them, **Ember Theme**, holds everything
about how the storefront looks. Another, **Lookbook**, configures the shoppable-scenes
page. The remaining seven are `i18n.*` sections holding storefront wording, which
BigCommerce fills from the theme's language files — most stores never open them.

## Dark Mode

Ember Theme has a real dark mode, not an inverted filter. Both palettes are designed.

| Setting | Effect |
| --- | --- |
| **Theme Mode** | `System` follows the visitor's operating system preference, `Light` and `Dark` force one. Default: `System`. |
| **Dark Toggle** | Shows a toggle button in the header so visitors can override whatever the default was. |

A visitor's choice is remembered in their browser and survives page loads. The theme sets
the mode before the page paints, so there is no flash of the wrong palette on load.

## Colors

Five colours drive the whole storefront. Every component derives from them, so you do not
need to restyle pieces individually.

| Setting | Used for |
| --- | --- |
| **Accent** | Highlights, sale flags, active states |
| **Primary** | Buttons, links, anything the shopper is meant to click |
| **Heading** | Headings |
| **Text** | Body copy |
| **Muted** | Secondary copy, captions, metadata |

Two more sit beside them: **Accent text**, the accent as used for text (often a shade
darker than the accent itself, so it stays readable on white), and **Button**, the fill of
the primary buttons.

**Dark Mode Colors** repeats the same set for dark mode. Dark mode reads only these, so a
colour changed under **Colors** does not carry over to it.

Each variation ships a palette that meets WCAG AA contrast in both light and dark mode. If
you change these values, check the result in both modes — a colour that reads well on white
often fails on the dark surface.

### Primary button colour

Primary buttons — Add to Cart, Checkout, Sign In, Apply — take their fill from
**Ember Theme → Button** in light mode and **Dark Mode Colors → Button** in dark mode. Hover
and pressed shades are mixed from it, so one colour is all you set.

The standard Cornerstone controls under **Buttons and icons → Primary action button** still
work, in light mode, and take over once you change them:

| Setting | Counts as "not set" at | When you change it |
| --- | --- | --- |
| **Button background** | `#1B1D21` | Replaces the Button colour; hover and pressed shades are mixed from it |
| **Button background hover** | `#333333` | Replaces the mixed hover shade |
| **Button background active** | `#000000` | Replaces the mixed pressed shade |

!!! note "Three values mean “use the theme’s colour”"
    Those three values are what the theme ships with, and a control left at its shipped
    value is treated as untouched — so the theme's own Button colour paints the buttons.
    That means choosing *exactly* `#1B1D21` for the background, `#333333` for hover or
    `#000000` for pressed changes nothing. If one of those is the colour you want, pick
    one a step away, such as `#1B1D22` or `#010101`; nobody can see the difference.
    **Button text color** has no such rule and always applies. None of the Cornerstone
    button controls has a dark-mode twin: in dark mode, use **Dark Mode Colors → Button**.

## Layout

| Setting | Options | Default |
| --- | --- | --- |
| **Background** | colour | — |
| **Surface** | colour used for cards and panels | — |
| **Border** | colour | — |
| **Max Width** | 1200px, 1400px, 1600px | 1400px |
| **Border Radius** | 0px, 8px, 14px, 20px | 14px |

Border Radius applies globally — buttons, cards, inputs, images. `0px` gives a hard-edged
look; `20px` is soft and rounded.

## Typography

Fonts are chosen with the standard Cornerstone controls: **Global → Body text and links →
Body text font family** and **Global → Headings → Heading font family**. The theme's
heading scale adapts to whichever family you pick.

Each variation ships a pair:

| Variation | Body text | Headings |
| --- | --- | --- |
| **Home** | Plus Jakarta Sans | Plus Jakarta Sans, at weights 700 and 800 |
| **Fashion** | Jost | Playfair Display |
| **Food** | DM Sans | Fraunces |

Each font offered by those two controls loads every weight the theme draws it at — for body
text, regular through extra-bold plus italic — so bold text comes from the real bold cut
instead of being thickened by the browser. (The checkout's own font controls are separate
and unchanged.)

!!! warning "Upgrading from an earlier build? Pick your fonts again"
    Earlier builds saved a font with a single weight, for example
    `Google_Plus+Jakarta+Sans_400`. A saved setting is kept when you upgrade, so a store
    that still has one of those loads that one weight only, and every bold heading, price
    and button label is faked by the browser. Open both font controls, select your font
    again and save; the setting is rewritten with every weight, for example
    `Google_Plus+Jakarta+Sans_400,500,600,700,800,400italic`. If the dropdown already
    shows your font, pick a different one first and then yours, so the editor registers a
    change.

## Announcement bar

Up to three rotating messages across the top of every page. Leave a message empty to skip
it; leave all three empty to hide the bar.

## Mega menu

Two promotional slots inside the navigation dropdowns, each an image plus a link: one under
**Categories**, one under **Shop**. There is also a banner image and text for the
All Categories panel.

## Homepage

| Block | Controls |
| --- | --- |
| **Hero and footer pills** | The three short notes under the hero buttons and in the footer: `Built-in text (translated)`, `Your text below` (**Pill 1** to **Pill 3**; an empty pill is hidden; `{amount}` shows your free-shipping amount, since 1.1.31) or `Hidden` (since 1.1.28; the footer follows it since 1.1.29, the cart page returns badge since 1.1.31) |
| **Trust badges** | On/off, plus a title and a line of text for each of three badges |
| **Promo banner** | On/off, one wide banner image, three supporting images, and an option to repeat the trust badges beneath; **Promo returns note** replaces the returns badge's note "Hassle free returns" (empty keeps it, since 1.1.29). Since 1.1.35 the banner shows only when it has somewhere to go: its link setting, or a top-level category named "Sale" |
| **Flash sale** | On/off, source (Best Sellers, Featured, or New Arrivals), title, text, and an end date that drives the countdown. The end date is empty by default since 1.1.35: no countdown and no "Hurry up" line until you set one |
| **Reviews** | On/off, an aggregate score and count, and three named quotes |
| **Newsletter** | On/off, title and text |
| **Brand story** | On/off |
| **Press bar** | On/off, a title, and five logo-plus-link slots |

### "View all" links (since 1.1.33)

Each product section on the home page (the Featured / Best Sellers / New Arrivals tabs or
shelves, and the Flash Sale) ends with a "View all" link when your store has somewhere to send
it. The theme looks, in this order, for:

1. a category named for the section: **Featured**, **Best Sellers**, **New Arrivals**, or
   **Sale** for the Flash Sale;
2. a category named **Shop All**, opened sorted to match the section (featured, best selling
   or newest; the Flash Sale follows its source);
3. a top-level category whose name starts with "Shop All", in any case (for example
   "Shop All Store 2"), sorted the same way;
4. your only top-level category, if the store has just one, sorted the same way.

With none of these the section shows no link. To choose where a section's link goes, give a
top-level category that section's name.

### Hero pills

The built-in pills read "Free shipping" (only while **Free Shipping Messages** is on with an
amount) and "Secure checkout", in the shopper's language. Since 1.1.35 there is no built-in
returns pill: the theme cannot know your returns policy. To state one, or if your store charges
shipping on some or all orders, set **Hero and footer pills** to `Your text below` and write
them (for example "Free shipping on many pieces", "30-day returns"), or choose `Hidden`. The choice applies to every hero slide,
including slides built from **Storefront > Carousel**, and to the three pills in the footer.
On phones the hero pills are not shown. With `Your text below` or `Hidden`, the theme's own
first hero slide (Home style) also drops its "fast shipping and hassle-free returns" line.

**Your free-shipping amount in a pill (since 1.1.31).** Type `{amount}` where the amount goes,
for example `Free shipping over {amount}`. The pill then shows your **Free Shipping ($)**
amount (Theme Editor > Cart) in the shopper's currency, the same way the top bar's default
message does: a shopper browsing in euros reads "Free shipping over €184", not "$200". While
**Free Shipping Messages** is off, or the amount is 0, a pill containing `{amount}` is hidden.
Type the amount yourself instead ("Free shipping over $150") and it stays in your store's
currency for every shopper.

**Pill 2 is your returns promise (since 1.1.31).** With `Your text below` the cart page's returns
badge reads your **Pill 2**, so one edit changes the returns promise in the hero, the footer and
the cart; the home trust badges, the promo banner row and the product page's "Easy Returns" line
show only while Pill 2 does (since 1.1.35). Pill 2 is empty by default, and `Built-in text` and
`Hidden` show no returns badge or line.

### Hero focus on phones and tablets

The hero photographs are wide, and below 1100px the hero box is much narrower than the
picture, so the photo is cropped to fill it. **Hero 1 Focus**, **Hero 2 Focus** and
**Hero 3 Focus (phones & tablets)**, one per slide, choose which part of the width stays
in view: `0% (left)` keeps the left edge, `50% (centre)` crops evenly from both sides,
`100% (right)` keeps the right edge, in steps of 10%. Set each one to where the subject of
that slide stands. Desktop always shows the centred crop.

| Variation | Hero 1 | Hero 2 | Hero 3 |
| --- | --- | --- | --- |
| **Home** | 50% | 50% | 50% |
| **Fashion** | 80% | 90% | 90% |
| **Food** | 70% | 80% | 80% |

These are the values each variation ships with, chosen for its own photographs. A slide
replaced through Page Builder (see [Replacing the homepage hero](page-builder.md#replacing-the-homepage-hero))
is your own widget, and its focus setting does not apply to it.

## Category pages

**The category header.** The category image you set in BigCommerce sits in the header at
the top of that category's page. **Global → Products → Category header with an image**
picks how:

| Option | Effect |
| --- | --- |
| **Banner: photo behind the title** (default) | The photo fills the header and the breadcrumb, title and description sit on it, over a shade that keeps the text readable |
| **Split: title beside the whole photo** | The title and description sit beside the image, which is shown whole (before 1.1.37 the Fashion style started on Split; every style now starts on Banner) |

With **Split**:

- From 600px wide, the title and description are on the left and the image on the right at
  a fixed height: 240px on desktops, 200px on tablets. The image keeps its own shape and is
  not cropped; a very wide image (wider than about 2:1) is shrunk to fit instead.
- On phones the image sits under the title, 180px tall.
- A category with no image, or no description, shows only what it has.

!!! tip "Choosing a category image"
    Any shape works, because nothing is cropped. A landscape image between 4:3 and 2:1
    uses the space best. Upload it at least 1000px wide so it stays sharp on
    high-density screens.

**Filters.** The Clear button in the filter sidebar appears only once a filter is set. A
store without product filtering shows a compact Shop By Price block instead.

## Product pages

| Setting | Effect |
| --- | --- |
| **Sticky ATC Bar** | Keeps an add-to-cart bar visible as the shopper scrolls past the buy box |
| **Q&A Tab** | Adds a questions tab to the product tabs |
| **Compare button outside category and brand pages** | Shows the compare button on product cards. Turned off, no card shows it, category and brand pages included; turned on, those two pages also need BigCommerce's own product comparison setting |
| **Show quickview button on product cards** | Shows the Quick View button on product cards. Turned off, no card shows it anywhere; turned on, it also shows on touch tablets 768px and wider, where it is always visible instead of appearing on hover. Touch phones never show it |

The share buttons under the product follow the social sharing buttons ticked in the control
panel, in the same order, including Print and the Facebook Like button. Untick them all and the
product page shows no share row.

**Specifications.** The Specifications tab lists the product's custom fields
(**Products > Edit > Custom Fields**), with weight and dimensions when the store shows them.
Two kinds of field are left out, here and on the compare page:

- a field whose name starts with two underscores (`__`), such as `__CHASSIS NUMBERS` or
  `__@RENAME RAM`. Apps and merchants use this convention for settings that are not product
  facts; name a field this way to keep it off the storefront;
- `yen_badge`, which sets the card badge (new, sale, sold out), and fields whose value is
  empty or a dash.

A long value, such as a web address, wraps inside its own column.

**Reviews.** The Reviews tab, the "N reviews" link beside the stars and the review summary
count the reviews the tab lists. If BigCommerce counts reviews it does not list on this
storefront (for example reviews not yet approved), the stars still follow BigCommerce's
rating, but the tab shows no count and the link is left out until a review can be listed.

**Buttons in your description.** Links you give the class `button` in a product description
or warranty (Cornerstone's button style) take the theme's button look and fill with your
accent tint on hover.

**Product photos on cards.** Product cards show the whole photo, centred on the card's light
ground. A photo the shape of the card (square, or 3:4 with the Fashion style) fills it; a
wider or taller one is not cropped and leaves even bands. For the fullest cards, upload
square photos (3:4 with the Fashion style), at least 1000px wide. The second photo shown on
hover always fills the card.

## Cart

| Setting | Effect |
| --- | --- |
| **Free Shipping ($)** | The threshold the shipping progress bar counts toward: 25, 50, 75, 100, 150, or 200 |
| **Free Shipping Messages** | Shows the free-shipping amount wherever the theme mentions it: the top bar's default first message, the cart sheet, the product page, the cart page (progress card and "Free ship" badge) the note under **Free Shipping** in the home promo banner and the free-shipping perk on the Account created page (since 1.1.29). Turn it off to hide all of them (called **Shipping Bar** before 1.1.27, when it hid only the cart page card). Off by default since 1.1.34: turn it on once your shipping rules offer free shipping over an amount |
| **Cross-sell** | Shows related products in the cart |
| **Trust Badges** | Shows the badges in the cart: free shipping (with **Free Shipping Messages**), returns (follows **Hero and footer pills**, Pill 2, since 1.1.31) and secure checkout |
| **Recently Viewed** | Shows a recently-viewed strip, with a configurable item count |

Set the **Free Shipping** threshold to match the free-shipping rule you configured in
**Settings → Shipping**. The theme does not read your shipping rules; it only draws the bar.

Below the threshold, the cart page, the cart sheet that opens after Add to Cart, and the
product page all say how much is still missing — "Add $12.00 more for free shipping" —
in the shopper's currency. Once the cart reaches it, the shipping row reads **FREE**.

If your store ships free on every order, or has no free-shipping offer, turn **Free
Shipping Messages** off (since 1.1.27). A **Free Shipping** amount of 0 is treated the same
way. With the messages off and the first top-bar message left empty, the top bar starts
with its second message; to say "Free shipping on every order" there, type it into the
first top-bar message.

The cross-sell row on the cart page leaves out products that are already in the cart. If
that leaves fewer products than the row holds, it shows the ones that remain.

## About page

Settings for the page that uses the **About** template (since 1.1.25).

| Setting | Effect |
| --- | --- |
| **Story photo (Image Manager file name)** | Your own Our Story photo: the file name of an image uploaded in **Storefront > Image Manager**. Empty: the theme's photo for your style. |
| **Story photo description (alt text)** | What a screen reader says for your photo. |
| **Stats** | `Built-in text (translated)`, `Your text below` (the four number and label pairs) or `Hidden` (the default since 1.1.34, so a new store shows no figures it has not typed). |
| **Values** | The same three choices for the six value cards (title and text each); `Hidden` by default since 1.1.34. |
| **Hero sentence and closing banner** | `Built-in text (translated)` or `Your text below`: **Hero sentence**, **Banner title**, **Banner text**, **Button label** and **Button link** (a page of your store, such as `/shop-all/`; since 1.1.26). |

With **Your text below**, an empty number or title hides that item, and the section
disappears when all of them are empty; an empty hero sentence or banner field hides that piece.
Details and examples:
[The other page templates](page-templates.md#about).

## Payment icons

**Header and footer → Payment icons** has one checkbox per payment method: American Express,
Discover, Mastercard, PayPal, Visa, Amazon Pay, Apple Pay, Google Pay and Klarna. The icons
you tick show in the footer, the cart, the product page and the cart drawer. **Show Apple
Pay** (new in 1.1.13) starts off, so turn it on if your store accepts Apple Pay.

## Prices hidden from guests

BigCommerce can hide prices from shoppers who are not signed in. That is a store setting,
not a theme one, and the theme follows it everywhere it prints a price. For a guest on such
a store, Ember shows no price on:

- product cards, wherever they appear
- the product page, its bulk pricing table and its fixed shipping cost
- the free-shipping progress bar in the cart (the threshold sentence stays, the bar and the
  amount still missing do not)
- the structured data (JSON-LD) search engines read from the product page

!!! info "What this means for search results"
    The theme leaves the whole `offers` block out of the structured data for guests, since
    an offer without a price is an error in Google's Rich Results test. Search engines crawl
    as guests, so Google has no price or availability to show in a rich result for your
    products. That is the trade-off of hiding prices from guests. Signed-in shoppers see
    every price as usual.
