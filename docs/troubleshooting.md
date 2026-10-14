# Troubleshooting

**A Lookbook product card is missing.** The ID is wrong, or the product is not visible on
the storefront. Check the ID in **Products → View**, and check the product is visible and
in stock behaviour you expect.

**A hotspot sits in the wrong place.** Coordinates are percentages, not pixels, and they
are measured against the image, not the screen. Re-check the pair order — dots map to
product IDs by position.

**Colours look wrong after switching variation.** Switching applies that variation's
settings over yours. Set the variation first, then customise.

**Dark mode ignores a colour I changed.** Dark mode has its own palette under
**Theme Editor → Ember Theme → Dark Mode Colors**, and a colour changed under **Colors** does
not carry over to it. Set both, and preview both modes before publishing.

**The hero cuts off the person or product on a phone.** The photograph is cropped to fit
the narrow screen. Move the crop with **Theme Editor → Ember Theme → Hero N Focus (phones &
tablets)** — see [Hero focus](usage/theme-editor.md#hero-focus-on-phones-and-tablets).

**I set a primary button colour and nothing changed.** Each Cornerstone primary button
control has one value the theme treats as "not set": `#1B1D21` for the background,
`#333333` for hover, `#000000` for pressed. Pick a colour one step away, such as `#1B1D22`,
or set **Ember Theme → Button** instead — see
[Primary button colour](usage/theme-editor.md#primary-button-colour).

**Bold text looks smudged or too thin after an upgrade.** The saved font setting loads a
single weight. Pick the font again — see [Typography](usage/theme-editor.md#typography).

**Guests see no prices, and Google shows none either.** The store is set to hide prices
from guests, and the theme leaves prices out of the page and its structured data too — see
[Prices hidden from guests](usage/theme-editor.md#prices-hidden-from-guests).

**A homepage section will not appear.** Most sections have an on/off checkbox in
**Theme Editor → Ember Theme**, and several also hide themselves when their content fields
are empty.
