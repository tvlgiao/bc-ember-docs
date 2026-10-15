# Page Builder

Ember Theme exposes 35 Page Builder regions. Open **Storefront → Page Builder**, pick a page,
and drag widgets into the highlighted drop zones.

## Replacing the homepage hero

The three hero slides are Page Builder regions: `home_hero_slide_1`, `home_hero_slide_2`,
and `home_hero_slide_3`. Dropping a widget into one **replaces** that slide's built-in
content entirely, which is how you use a custom hero without editing theme files. Leave a
region empty and the theme renders its own slide.

The hero slots are used only when the store has no Storefront → Carousel slides, or when
Theme Editor → Ember Theme → Homepage → *Hero: Storefront > Carousel slides* is off. While that
setting is on and Control Panel carousel slides exist, the hero is built from those slides
instead.

## Above the products and above the footer

Two more homepage regions take widgets of your own between the theme's blocks:

- `home_above_products` sits directly above the first product feed: above the Featured / Best
  Sellers / New Arrivals tabs in the Home and Fashion variations, and above the New Arrivals
  shelf in Food, where the feeds are shelves.
- `home_above_footer` sits at the end of the homepage, just above the footer.

Both are empty by default, so the homepage looks the same until you drop a widget in.

## All regions

| Page | Regions |
| --- | --- |
| Home | `home_hero_slide_1`, `home_hero_slide_2`, `home_hero_slide_3`, `home_below_menu`, `home_below_carousel`, `home_below_featured_products`, `home_below_top_products`, `home_below_new_products`, `home_above_products`, `home_above_footer` |
| Category | `category_below_header`, `category_below_content` |
| Product | `product_below_price`, `product_below_shipping`, `product_below_content`, `product_questions`, `product_item_below_price` |
| Cart | `cart_below_totals`, `cart_below_crosssell`, `cart_below_content` |
| Search | `search_above_content`, `search_below_content` |
| Brand | `brand_below_header`, `brand_below_content` |
| Brands list | `brands_below_header`, `brands_below_content` |
| Blog | `blog_below_header`, `blog_below_content` |
| Blog post | `blog_post_below_header`, `blog_post_below_content` |
| CMS page | `page_builder_content` |
| Every page | `header_bottom`, `header_bottom--global`, `header_navigation_bottom--global`, `ssl_site_seal--global` |

Regions ending in `--global` appear on every page at once, so a widget dropped there does
not need repeating per page.
