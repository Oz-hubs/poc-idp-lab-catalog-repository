# shop-events-bus

Message broker (Kafka-like) used to publish and consume domain events across services.

- **Type:** message-broker
- **Used by:** `shop-orders-service`, `shop-inventory-service`, `shop-notification-service`

## Topics (example)

- `orders.created`
- `orders.shipped`
- `inventory.low`
