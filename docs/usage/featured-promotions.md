# Featured Promotions

A featured promotion shows a short callout, such as "Buy 2, save 15%", under the price of
every product it applies to, so shoppers see the offer before they reach the cart.

## Where the callouts appear

| Place | What shows |
| --- | --- |
| Product cards: category, brand and search pages, home page sections, related products, quick search | The top promotion, plus "+N more offers" when there are more |
| Product page and quick view | Every featured promotion for the product, in your priority order |
| Lookbook product strip | The top promotion, plus "+N more offers" |

Products without a featured promotion show nothing extra: no empty space, no gap.

## Featuring a promotion

The callouts come from BigCommerce, not from a theme setting:

1. In your control panel, create or edit an **automatic** promotion. Coupon promotions
   can't be featured.
2. Tick **Feature promotion** and enter the callout message (under 80 characters). The
   promotion has to name specific products in its conditions or rewards; a discount on
   the order subtotal alone can't be featured.
3. Save. A store can feature up to five promotions. Their order is set on the
   promotions' **Manage Priority** page.

BigCommerce does not check the callout against the promotion's rules, so write any
condition into the text yourself. Storefront pages are cached, and a change can take up
to 10 minutes to show.

## Theme setting

**Theme Editor → Theme Styles → Products → Featured promotions**

| Setting | What it does |
| --- | --- |
| **Show promotion callouts on product cards and product pages** | On by default. Turn it off to hide every callout. |
| **Callout background (light mode)** | The chip's background colour |
| **Callout text (light mode)** | The chip's text colour |

Each variation starts with its own pair (Home orange, Fashion brass, Food terracotta). In
dark mode the callout takes its colours from **Dark Mode Colors**, so it stays readable
on the dark page; the two colours above apply to light mode only. If you change them,
keep the text dark enough to read on the background.

## If no callouts appear

!!! note "BigCommerce is rolling this out store by store"
    BigCommerce is enabling featured promotion data one store at a time. Until it is on
    for your store, the storefront receives no featured promotions, so no callouts
    appear, even with a featured promotion set up and the setting on. Nothing else on
    the page changes. Once BigCommerce enables the data, the callouts appear without any
    theme change.

Also check that:

- the promotion is enabled, inside its date range, and ticked as featured;
- the product is one the promotion names;
- **Show promotion callouts…** is on in Theme Styles;
- 10 minutes have passed since the last change.
