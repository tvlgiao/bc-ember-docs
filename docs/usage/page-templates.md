# The other page templates

Ember Theme ships four custom page layouts. The Lookbook is covered above; the other three
work the same way — create a web page under **Storefront → Web Pages**, then pick the
template from the dropdown on that page's edit screen.

All three share one thing worth knowing before you start: **most of what you type into the
web page body is not what appears**. Each template renders its own content, so the page you
create supplies the URL and the template choice. This is the same arrangement as the
Lookbook, for the same reason — the layouts are designed, not free-form. The one exception is
the About page's Our Story section, below.

## About

Choose the **About** template. The page has six parts: a heading with your store name and a
sentence under it, four statistics, Our Story (text and photo), six value cards, the team and a
closing call to action.

!!! tip "Our Story is your own text"
    The **Our Story** section shows the text you write for the About Us page in
    **Storefront > Web Pages** (since 1.1.24). With no text it keeps the built-in copy. Write a
    paragraph or two about your store; you can use headings, lists and links. The "Our Story"
    heading stays as it is.

### Statistics, value cards and the photo (since 1.1.25)

Open **Storefront > Themes > Customize > Ember Theme > About page**.

**Stats** and **Values** each have three choices:

| Choice | What the page shows |
| --- | --- |
| Built-in text (translated) | The theme's sample figures ("50K+ Happy Customers" and so on) and value cards, in the shopper's language. This is the default, and what earlier versions showed. |
| Your text below | The fields under it: a number and a label for each of the four stats, a title and a short text for each of the six cards. Leave a number or a title empty to hide that item; the rest close up. Leave all of them empty and the section is not shown. |
| Hidden | No stats section, or no values section. |

The sample figures do not describe your store, so before the page goes live either switch
Stats to **Your text below** and enter figures that are true for you (for example `30` /
`Days to return`, `Free` / `Shipping over $50`), or choose **Hidden**. The fields start filled
with the sample text, so you only change what you need. Each field holds up to 64
characters. Each card keeps its icon (target, tag, globe, headset, leaf, shield, in that
order), so write the cards to fit them or leave the ones that do not fit empty.

Text you enter is shown as written in every language. If your store serves several
languages, the built-in choice is the one that is translated.

**Story photo.** By default the photo matches your theme style: a living room for the
Home style, a clothes rail for Fashion and pantry jars for Food. To use your own:

1. Upload the photo in **Storefront > Image Manager**. A landscape photo of at least 1200 px
   wide works best; it is shown about 16:9 and cropped to fill the frame.
2. Enter its file name in **Story photo (Image Manager file name)**, for example
   `about-us.jpg`. Pasting the image's path or URL from Image Manager also works.
3. Describe the photo in **Story photo description (alt text)** for screen readers, or
   leave it empty if the photo is only decoration.

The theme serves the photo from the BigCommerce image CDN at the size each screen needs. A
link to an image on another website is ignored and the default photo is shown instead.

### Hero sentence and closing banner (since 1.1.26)

The sentence under the page heading ("We're on a mission to bring quality products to
everyone, everywhere...") and the closing banner ("Ready to Shop?" with its **Shop Now**
button) share one setting in the same group, **Hero sentence and closing banner**:

| Choice | What the page shows |
| --- | --- |
| Built-in text (translated) | The theme's sample sentence and banner, in the shopper's language, with the button opening the store's category list (`/categories`). This is the default, and what earlier versions showed. |
| Your text below | **Hero sentence**, **Banner title**, **Banner text**, **Button label** and **Button link**. Leave one empty to hide that piece; leave the banner's title, text and button label all empty to remove the banner. |

**Button link** takes a page of your store: a path such as `/shop-all/` or `/sale/`, or the
full address of a page on your store (starting with your store's own address, for example
`https://yourstore.com/shop-all/`). A link to another website, or anything that is not a
link, opens `/categories` instead. Each field holds up to 64 characters.

The sample sentence speaks of shipping "everywhere"; if you ship to a few countries only,
choose **Your text below** and write a sentence that is true for your store.

The store name is substituted automatically wherever it appears, so it stays correct if you
rename the store.

## FAQ

Choose the **FAQ** template. It renders thirteen questions grouped into five categories,
with a search box and category filter that appear once the page loads.

The questions and answers are language-file content, under keys beginning `faq.`. The
sample text describes a generic store — free shipping over a threshold, a thirty-day
return window, a list of accepted cards — and **none of it is true of your store until you
change it**. Read through it before the page goes live.

Two things follow from the content living in the language file:

- the page is translated into all twenty languages the theme ships, so a shopper on a
  non-English storefront reads the FAQ in their own language
- the same text feeds the page's structured data, so a search engine is told exactly what
  a visitor sees — change one and the other follows

## Editing language-file content

The FAQ page, and the About page's headings, team and built-in statistics, value cards, hero
sentence and closing banner,
take their words from `lang/`, and each language has its own
complete copy: `lang/en.json`, `lang/de.json`, `lang/ja.json` and so on. Editing
`lang/en.json` changes the English storefront and nothing else.

If your store serves more than one language, every locale you have enabled needs the same
edit. The theme ships translations of the sample text, so those pages read correctly out of
the box — but the moment you replace the samples with your own policies, the other
languages still describe the samples until they are updated too.

## Track Order

Choose the **Track Order** template. It tells a shopper where their orders are and what the
five order stages mean.

It deliberately does **not** offer an order-number lookup form. BigCommerce provides no
storefront endpoint a theme can query for a guest's order, so a form asking for an order
number and an email could not do anything with them. What the page offers instead is what
actually works:

- a signed-in shopper gets a link to their order history, where every order carries its
  status and, once it ships, its tracking link
- a guest is told that a tracking link is emailed when the order ships, and is offered
  sign-in — or, if they checked out as a guest, a password reset using the address they
  gave at checkout, which is BigCommerce's own route to an order history
