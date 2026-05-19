# shop-inventory-service

Tracks stock levels for products.

- **Type:** service
- **Provides:** `shop-inventory-rest-api`
- **Consumes:** `shop-orders-rest-api`
- **Depends on:** `shop-events-bus`

## Responsibilities

- React to order events (decrement stock).
- Expose stock-level queries.
