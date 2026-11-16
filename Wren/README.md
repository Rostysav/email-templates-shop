# Wren after-delivery emails

Six dark HTML emails for the weeks after a Shopify order arrives: delivered, care, review, reorder, a friend code, and a win-back note. Names, the The Cedar Candle price, and the code `WREN15` are examples. Replace them before you send.

Open `index.html` in a browser to view the set. That page is only a local index. Do not email it.

Each letter uses tables and inline CSS for Gmail, Apple Mail, Outlook, Yahoo, and mobile mail apps. The colors are locked so a dark-mode inbox does not repaint them.

## Files

| File | Send it when |
| --- | --- |
| `delivered.html` | The parcel is marked delivered |
| `care.html` | A day later, with how to use the product |
| `review-request.html` | About a week after delivery |
| `reorder.html` | The product is likely running low |
| `referral.html` | You want a customer to invite a friend |
| `win-back.html` | They have not ordered again in a long while |

## Change the brand

The mark is the letter `W` in a box, then the word `WREN`. Both are text. The word appears again in the footer.

1. Replace `W` with your initial, or remove that cell and use a hosted logo.
2. Replace both `WREN` words with your store name. Also change the codes `WREN15` and `AGAIN`.
3. Replace the footer address (90 Yesler Way, Seattle, WA 98104) and the copyright line.
4. Rewrite the product name, price, and care steps for what you actually sell.

## Change the links

Every link inside a letter is `href="#"`. Search for it and point each one at the real page. The unsubscribe link has to be the link your sending tool provides.

## Change the images

Photo areas use a flat background plus a small PNG from placehold.co. Host your own image and replace each `src`. Leave the `background-color` so the block still holds if the image is slow.

## Where these letters go

This pack starts after delivery. It does not replace a welcome email or an order confirmation.

`delivered.html` can follow Shopify’s shipping notification, or a flow that triggers when the carrier marks the parcel delivered. The other five are campaign letters. Send them from Shopify Email, Klaviyo, or a reviews and referrals app, and use that tool’s own merge tags for the name, product, and code.

## Before you send

1. Preview `index.html`, then open the letter you changed.
2. Replace example copy, `#` links, and placehold.co images.
3. Send a test to Gmail. Check Apple Mail and Outlook if you can.

Images in a real send must be `https` URLs on a host you control.
