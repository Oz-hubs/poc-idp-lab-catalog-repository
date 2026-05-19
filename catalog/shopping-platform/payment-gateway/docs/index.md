# payment-gateway

Third-party payment gateway provider (external vendor, managed outside the organization).

- **Type:** service (external)
- **Lifecycle:** production
- **Provides:** `payment-gateway-api`

## Notes

- This Component models an external vendor so the `payment-gateway-api` has a proper provider relation in the catalog.
- No source code is owned by the organization — it represents a SaaS dependency (e.g. Stripe).
- Used by `shop-orders-service` to charge customers during checkout.
