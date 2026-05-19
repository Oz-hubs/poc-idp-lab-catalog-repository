# shop-catalog-service

Backend service that exposes the product catalog.

- **Type:** service
- **Provides:** `shop-catalog-rest-api`
- **Depends on:** `shop-catalog-db`, `shop-shared-lib`

## Responsibilities

- Manage products and categories.
- Serve product listings and details to `shop-web` and `shop-admin-web`.
