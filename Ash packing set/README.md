# Ash packing set

Three papers for the box: a packing slip, a thank-you card, and a return note. The names, the Hudson address, order #1044, and the three products are examples so you can see the design. Replace them before you print a real order.

Open `index.html` in a browser to preview the set. That page stays on your computer. Do not put it in a parcel.

## Files

| File | Use it for |
| --- | --- |
| `packing-slip.liquid` | The slip Shopify prints with an order |
| `packing-slip.html` | A filled sample of that slip, for preview and for a printer |
| `thank-you.html` | A 5 × 7 inch card |
| `return-insert.html` | A 5 × 7 inch return note |

## Install the packing slip

1. In Shopify admin, go to **Settings → Shipping and delivery**.
2. Under **Documents**, open **Packing slip template**.
3. Replace the template with the contents of `packing-slip.liquid`.
4. Click **Preview template**, then **Save**.
5. Print one real order and read it before you use it on a busy day.

Shopify fills the shop name, the addresses, the order number, the date, and the items. A partial shipment prints the quantity in this box, for example `1 of 3`, and a line that the rest of the order is not in the parcel. An order note prints under **A note** when the order has one.

Prices are not on the slip. Shopify does not pass item prices into the packing slip template. This sheet is the list of what is in the box, not an invoice.

Product photos come from the order. Shopify only allows images from its own files. A logo file, if you add one, has to be uploaded on the **Files** page in the admin.

## Print the card and the return note

Open `thank-you.html` or `return-insert.html`. Click **Print**. Set the paper to **5 × 7 in** and turn on background graphics if you want the warm paper color. The type is drawn, so the card still reads on plain white paper.

You can also choose **Save as PDF** in the print dialog and hand that file to whoever packs the orders.

These two pages are not wired to an order. Print a stack, and put one of each in the box.

## Change the brand

The mark is the letter `A` in a box, then the word `ASH`. Both are text.

1. In every file, replace `A` with your initial and `ASH` with your store name.
2. Replace `Goods for the house` in `packing-slip.liquid` and `packing-slip.html`.
3. On the card and the return note, replace the Hudson address, `hello@ash.example`, and the fourteen-day window.
4. Rewrite the sentences so they sound like your shop.

On the live slip, **From**, the footer domain, and the footer email come from Shopify settings. The wordmark does not. If the store name in Shopify is already right, you still change `ASH` yourself.

The sample slip shows Helen Cho, 18 Grove Street, Hudson, NY 12534, order #1044, and three products. Those exist only in `packing-slip.html`. They are not in the Shopify file.
