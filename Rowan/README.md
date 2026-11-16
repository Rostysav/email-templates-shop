# Rowan drop emails

Six dark HTML emails for a small clothing drop: the waitlist, early access, the hour the page opens, a note while pieces remain, the last sizes, and a second cut. The Field Coat, the $265 price, the run of 40, and the name Mira Chen are examples. Replace them before you send.

Open `index.html` in a browser to view the set. That page is only a local index. Do not email it.

Each letter uses tables and inline CSS for Gmail, Apple Mail, Outlook, Yahoo, and mobile mail apps. The colors are locked so a dark-mode inbox does not repaint them.

## Files

| File | Send it when |
| --- | --- |
| `waitlist.html` | Someone joins the list for an upcoming drop |
| `early-access.html` | The list can buy before the public page opens |
| `drop-live.html` | The product page is open |
| `still-available.html` | Pieces remain and you have a real customer note |
| `last-sizes.html` | Only a few sizes are left |
| `back-in-stock.html` | You cut the same product again |

## Change the brand

The mark is the letter `R` in a box, then the word `ROWAN`. Both are text. The word appears again in the footer.

1. Replace `R` with your initial, or remove that cell and use a hosted logo.
2. Replace both `ROWAN` words with your store name.
3. Replace the footer address (1554 N Milwaukee Avenue, Chicago, IL 60622) and the copyright line.
4. Rewrite the product name, price, sizes, batch count, dates, and the quote for what you actually sell.

## Change the links

Every link inside a letter is `href="#"`. Search for it and point each one at the real page. The early-access link has to be the private URL your sending tool creates. The unsubscribe link has to be the link that tool provides.

## Change the images

Photo areas use a flat background plus a small PNG from placehold.co. Host your own image and replace each `src`. Leave the `background-color` so the block still holds if the image is slow.

## Where these letters go

This pack is a drop. It does not replace a welcome email, an order confirmation, or a shipping update.

Send the six from Shopify Email, Klaviyo, or the flow tool you already use. Time them off that tool: list signup, a scheduled send, the product going live, and inventory running low. Use the tool's own merge tags for the name, product, and link. The dates in these files are an example (early access Wednesday, November 18, 2026 at 8:00 a.m. ET, public page Thursday, November 19 at 10:00 a.m. ET).

## Before you send

1. Preview `index.html`, then open the letter you changed.
2. Replace example copy, `#` links, and placehold.co images.
3. Send a test to Gmail. Check Apple Mail and Outlook if you can.

Images in a real send must be `https` URLs on a host you control.
