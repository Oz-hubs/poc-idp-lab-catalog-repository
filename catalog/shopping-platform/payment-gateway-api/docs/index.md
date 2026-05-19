# payment-gateway-api

External payment gateway API (Stripe-like) consumed by `shop-orders-service`.

- **Type:** openapi
- **Lifecycle:** production
- **Consumer:** `shop-orders-service`

## Endpoints

| Method | Path       | Description     |
| ------ | ---------- | --------------- |
| POST   | `/charges` | Create a charge |

This API is **external**: the catalog only describes its contract for discoverability.
