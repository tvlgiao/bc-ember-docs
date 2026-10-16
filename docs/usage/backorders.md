# Backorders

With BigCommerce Backorders, shoppers can buy a product beyond the units you have on
hand, up to the backorder limit you set. The theme shows them what they are getting: how
many units will be backordered, and when you expect to ship them.

## What you set up in BigCommerce

Everything the theme shows comes from your store's settings; the theme has no backorder
setting of its own.

- **On each product:** its stock on hand and its backorder limit (or unlimited
  backorders), per variant where the product has variants.
- **Backorder messages:** the store's default message and any message you assign to a
  product, such as "Ships in 2–3 weeks".
- **Settings → Inventory:** which backorder details shoppers see: the backordered
  quantity, the backorder message, the availability prompt, the default
  shipping-expectation prompt, and the quantity on hand.

!!! note "Stock level display must not be “Don't show”"
    BigCommerce sends no backorder figures to the storefront while stock levels are
    hidden. With **Settings → Inventory → Stock level display** set to **Don't show**,
    the backordered quantities below do not appear, whatever the other backorder
    settings say.

## What shoppers see

| Page | What shows |
| --- | --- |
| **Product page and quick view** | The availability prompt, "N will be backordered" when the quantity chosen goes beyond what is on hand, and the product's backorder message (or your default message). Each line follows its own Settings → Inventory switch. |
| **Quantity limit** | Above the most that can be ordered (on hand plus the backorder limit), Add to Cart is disabled with "The maximum purchasable quantity is N". Lowering the quantity turns it back on. |
| **Nothing on hand** | A product that can still be backordered keeps Add to Cart. It shows as sold out only when nothing can be ordered at all. |
| **Options and pick lists** | Each variant and each pick-list option follows its own stock, limit and message. |
| **Cart page and cart panel** | Under each line's quantity: "N ready to ship" (only when part of the line is backordered), "N will be backordered" and the backorder message, with a group per pick-list option. The cart summary adds your shipping-expectation message when the cart holds a backordered item. |
| **Account → Orders → order details** | The backordered quantity and message under the product name, and your shipping-expectation message under the shipping address. |

While any unit is backordered, the product page drops its "Get it by …" delivery
estimate, because that date would not hold.

Lines with nothing to say are left out completely: a product that is fully in stock
shows no backorder box and no empty space.
