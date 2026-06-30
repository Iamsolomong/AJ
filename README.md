# Average Joe headless Shopify storefront

A modern, fast, conversion-focused headless storefront starter for Average Joe. It keeps Shopify as the commerce engine and uses a custom front-end for stronger brand experience, faster shopping and cleaner upsell/cross-sell flows.

## What this includes

- Modern homepage with mood-based shopping instead of generic collections.
- Product grid with quick size selection and quick add.
- Cart drawer with free-shipping upsell messaging.
- Bundle section for 2 tees, tee + hoodie and gifting.
- Product detail page template with related-product cross-sell area.
- Shopify Storefront API connection for products, variants and cart checkout.
- Fallback demo products so the site still runs before API credentials are added.

## Connect to Shopify

1. In Shopify, create a Storefront API access token for your store.
2. Copy `.env.example` to `.env.local`.
3. Set these values:

```bash
SHOPIFY_STORE_DOMAIN=not-today-susan.myshopify.com
SHOPIFY_STOREFRONT_ACCESS_TOKEN=your_storefront_access_token
SHOPIFY_API_VERSION=2026-04
```

4. Install and run:

```bash
npm install
npm run dev
```

5. Open `http://localhost:3000`.

## Shopify setup notes

For better merchandising, add product tags/metafields such as:

- `Workday`
- `Weekend`
- `Emotionally Fragile`
- `Gift`
- `Australia`
- `Best Seller`
- `Hoodie`

The homepage mood filters and related-product areas can use these tags to create faster shopping paths.

## Conversion structure

The redesign is built around these conversion moments:

1. **Hero = clear positioning + instant shopping.** No vague lifestyle line first. The first screen tells people what AJ is and gives two actions.
2. **Mood filters = faster discovery.** Customers shopping funny tees often shop by feeling, occasion or recipient, not just “men/women”.
3. **Quick add = fewer product-page dead ends.** Size buttons and add-to-cart happen from the collection grid.
4. **Cart drawer = AOV growth.** The cart nudges one more tee, free shipping or hoodie layer before checkout.
5. **Bundle blocks = intentional upsell.** The homepage sells combinations, not just single items.
6. **Hide empty proof.** Do not show `0.00 ★ (0)` reviews. Use real reviews later; until then use brand proof, guarantees or UGC-style quotes.

## Pages included

- `/` homepage
- `/products/[handle]` product detail template
- `/api/cart/create` API route that creates a Shopify cart and returns `checkoutUrl`

## Replace demo assets

Replace files in `public/previews/` with real product images or let Shopify images load automatically once the API connection is active.
