# shop-orders-service

Backend service that handles orders for the `shopping-platform` system.

- **Type:** service
- **Stack:** .NET (example)
- **Provides:** `shop-orders-rest-api`
- **Consumes:** `payment-gateway-api`
- **Depends on:** `shop-orders-db`

## Responsibilities

- Persist orders in PostgreSQL.
- Charge the customer through the external payment gateway.
- Expose a REST API used by `shop-web`.
