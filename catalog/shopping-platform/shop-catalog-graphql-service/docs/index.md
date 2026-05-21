# shop-catalog-graphql-service

GraphQL backend service for the shopping catalog domain.

## Responsibilities

- Expose the `shop-catalog-graphql-api` schema.
- Aggregate data from `shop-catalog-rest-api` and `shop-inventory-rest-api`.
- Provide a consumer-friendly query model for web clients.

## Dependencies

- `shop-catalog-service`
- `shop-inventory-service`
- `shop-shared-lib`

## Consumers

- `shop-web`
- `shop-admin-web`
