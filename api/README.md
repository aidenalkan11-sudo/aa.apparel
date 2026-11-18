# Stripe endpoint placeholder

When Stripe is ready, add `/api/create-checkout-session` as a server-side function. Read `STRIPE_SECRET_KEY` from environment variables and create a Stripe Checkout Session using the product ID posted by the frontend. Return `{ "url": session.url }`.