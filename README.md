# 2AA Apparel

Clean static storefront for 2AA. Four products are configured at A$40 each. Stripe is intentionally isolated behind a single checkout endpoint so Stripe keys can be added later without rebuilding the storefront.

## Stripe later
Create a Vercel/serverless endpoint at `/api/create-checkout-session` using the Stripe secret key in an environment variable. The frontend already posts `{ productId }` to that endpoint and expects `{ url }`, then redirects to the Stripe Checkout URL.

Never put `sk_...` keys in frontend code.