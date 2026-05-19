# shop-notification-service

Sends transactional emails to customers (order confirmation, shipping updates).

- **Type:** service
- **Consumes:** `shop-orders-rest-api`, `smtp-api`
- **Depends on:** `shop-events-bus`
