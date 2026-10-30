# Size Guide

The theme can show a **Size guide** link beside a product's size option, on the product
page and in quick view. The link opens your size chart in a pop-up, so shoppers check
their size without leaving the product.

## 1. Write the chart as a web page

Create the chart in **Storefront → Web Pages → Create a Web Page**, as you would any other
page. Tables, headings, lists and images all carry over into the pop-up; you can also
build the page with Page Builder.

- Give it a URL you will recognise, such as `/size-guide/`.
- Uncheck **Navigation menu** if you do not want it in your menus. The page only needs to
  exist; shoppers reach it through the link.

## 2. Point the theme at the page

In **Theme Editor → Products → Display settings**, enter the page's address in
**Size Guide Page URL**, for example `/size-guide/`, and save.

The link appears beside the first option whose name contains "size" (Size, Shoe Size, Ring
Size…), whatever way the option is displayed. Leave the field empty and no link is shown.

!!! note "Only pages on your own store"
    The address must be a page of this store (a path such as `/size-guide/`, or a full
    address on your own domain). An address on another site is ignored, because the
    page's content is placed inside your product page.

## 3. A different chart for some products (optional)

Give a product a custom field named **size_guide** (in **Products → edit → Custom
Fields**):

| Value | What happens |
| --- | --- |
| A page address, such as `/size-guide-shoes/` | That product shows this chart instead of the theme setting's. |
| `none` | That product shows no size guide link. |

The `size_guide` field is used only for the link; it is not listed in the product's
specifications or on the compare page.

## Good to know

- Wide tables scroll sideways on phones, so a chart with many columns stays readable.
- Pressing Escape closes the size guide only; a quick view behind it stays open.
- The link only checks the option's English name. If your size option is named in
  another language ("Größe", "Taille"), the link does not appear.
