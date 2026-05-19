# shopping-platform

Example e-commerce platform used to demonstrate Backstage catalog relationships.

## Components

- **shop-web** — React frontend.
- **shop-orders-service** — backend service that exposes the orders REST API.

## APIs

- **shop-orders-rest-api** — REST API exposed by `shop-orders-service`.
- **payment-gateway-api** — external payment gateway consumed by `shop-orders-service`.

## Resources

- **shop-orders-db** — PostgreSQL database used by `shop-orders-service`.

## High-level flow

1. The user browses `shop-web`.
2. `shop-web` calls `shop-orders-rest-api` on `shop-orders-service`.
3. `shop-orders-service` persists data in `shop-orders-db` and calls `payment-gateway-api` to charge the customer.

## Metadata Reference

For a comprehensive guide on all extractable metadata from this platform, see [metadata.md](../metadata.md).
