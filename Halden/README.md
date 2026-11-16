# Halden email templates

Six dark HTML emails for a Shopify store: welcome, abandoned cart, order confirmation, shipping, review request, and a Black Friday promo. Names, prices, the Mercer Street address, and the code `HALDEN10` are example copy so you can preview the design. Replace them before you send.

Open `index.html` in a browser to view the set. That page is only a local index. Do not email it.

Each letter is a single HTML file with table layout and inline CSS, so it can be read in Gmail, Apple Mail, Outlook, Yahoo, and mobile mail apps.

## Files

| File | Use it for |
| --- | --- |
| `welcome.html` | A new subscriber or first-order offer |
| `abandoned-cart.html` | Someone who left checkout |
| `order-confirmation.html` | Order confirmed |
| `shipping-update.html` | Parcel handed to the carrier |
| `review-request.html` | A review a week after delivery |
| `black-friday.html` | A short sale campaign |

## Change the brand

In every file, the mark is the letter `H` inside a gold box, then the word `HALDEN`. Both are text, not an image. The word appears again in the footer.

1. Replace `H` with your initial, or remove that cell if you will use your own hosted logo.
2. Replace both `HALDEN` words with your store name.
3. Replace the footer address (`48 Mercer Street`, `New York, NY 10013`) and the copyright line.
4. Rewrite the headline, body, discount code, and button label in that file.

To use an image logo, host a PNG and put it where the `H` cell is:

```html
<img src="https://your-cdn.example/logo.png" width="56" height="56" alt="Your store" style="display:block; width:56px; height:auto; border:0;">
```

## Change the links

Every link inside a letter is `href="#"`. Search each file for `href="#"` and point it at the real page: shop, cart, order status, tracking, review form, Instagram, privacy, unsubscribe.

The unsubscribe link has to be the one your sending tool provides. A literal `#` will not unsubscribe anyone.

## Change the images

Photo areas use a dark background color plus a small PNG from placehold.co, for example:

```html
<img src="https://placehold.co/88x88/212121/C6A36A.png?text=Coat" width="88" height="88" alt="The Wool Overcoat" ...>
```

Host your product and banner images on your own CDN (Shopify Files, Cloudinary, or similar) and replace each `src`. Update the `alt` text to the real product name. Leave `width`, `height`, and `background-color:#212121` in place so the layout holds if an image is slow or blocked.

placehold.co is only for preview. Do not send those URLs to customers.

## Change the colors

The same colors are repeated inline, because mail apps ignore a shared stylesheet. Search the file and replace both the `bgcolor` attribute and the matching CSS color.

| Role | Hex |
| --- | --- |
| Page background | `#0E0E0E` |
| Email card | `#161616` |
| Panels and image mats | `#212121` |
| Hairline | `#323232` |
| Main text | `#F3F0E8` |
| Secondary text | `#A8A29A` |
| Gold accent and button | `#C6A36A` |
| Text on the gold button | `#161616` |

If you change the gold, update the button background and the text color together so the label stays readable.

## Where to install each letter

This pack is a visual base. Example products and prices are not wired to a live store. Only two of the letters map onto Shopify’s built-in notification editor. The others are sent by a campaign or review tool, and that tool has its own merge tags.

### Order confirmation and shipping

In Shopify admin, go to **Settings → Notifications** and open **Order confirmation** or **Shipping confirmation** (use **Shipping update** if this second note is the one you send when tracking is added). Choose **Edit code**.

Keep any Liquid Shopify already marks as required, then replace the visible example text with the tags from that default template. Send yourself a test order from the admin before you rely on it. The usual tags are:

Order confirmation:

```liquid
{{ order.name }}
{{ order_status_url }}
{% for line in subtotal_line_items %}
  {{ line.image | img_url: 'compact_cropped' }}
  {{ line.title }}
  {{ line.quantity }}
  {{ line.final_line_price | money }}
{% endfor %}
{{ subtotal_price | money }}
{{ shipping_price | money }}
{{ tax_price | money }}
{{ total_price | money }}
{{ shipping_address | format_address }}
```

Shipping confirmation:

```liquid
{{ fulfillment.tracking_company }}
{{ fulfillment.tracking_numbers.first }}
{{ fulfillment.tracking_url }}
{% for line in fulfillment.fulfillment_line_items %}
  {{ line.line_item.title }}
  {{ line.quantity }}
{% endfor %}
```

Put the tracking URL on the **Track shipment** button. Put `{{ order_status_url }}` on **View your order**.

Check the default template in your admin before you paste. Shopify’s variable names belong to that notification, and a tag from one email will not resolve in another.

### The other four letters

| File | Send it from | What to swap in |
| --- | --- | --- |
| `welcome.html` | Shopify Email, Klaviyo, or another campaign tool | Your offer, code, and a link to the shop |
| `abandoned-cart.html` | The same tool, or Shopify’s abandoned checkout notification | That tool’s checkout link and line-item list |
| `review-request.html` | Your review app | That app’s product and review-form tags |
| `black-friday.html` | A campaign | Your sale copy, code, and collection link |

Abandoned checkout in Shopify notifications uses `abandoned_checkout`, not `order`. A promo email has no order line items, so leave those rows as the products you choose, or as the campaign tool’s product block.

## Before you send

1. Preview `index.html`, then open the letter you changed.
2. Replace example copy, `#` links, and placehold.co images.
3. Send a test to Gmail. Check Apple Mail and Outlook if you can.
4. Place a test order, or trigger the campaign, and confirm the live data appears.

Images in a real send must be `https` URLs on a host you control.

## `_build.mjs`

Edit the `.html` files. `_build.mjs` is the script that first generated them. Running `node _build.mjs` overwrites your edits in every letter.
