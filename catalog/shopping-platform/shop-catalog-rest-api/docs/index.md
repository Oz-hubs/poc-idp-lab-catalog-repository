# shop-catalog-rest-api

REST API exposed by `shop-catalog-service`.

## OpenAPI specification

The full OpenAPI definition is kept in a dedicated file and ingested by Backstage
via a `$text` placeholder, so the **Definition** tab of this entity renders the
exact same document via Swagger UI.

- Source file: [`openapi.yaml`](../openapi.yaml)
- In Backstage: open the entity `shop-catalog-rest-api` and switch to the **Definition** tab.

## Endpoints (summary)

| Method | Path             | Description                                              |
| ------ | ---------------- | -------------------------------------------------------- |
| GET    | `/products`      | List products (supports `category`, `limit` query params) |
| GET    | `/products/{id}` | Product detail                                           |
| GET    | `/categories`    | List categories                                          |

## Schemas

- `Product` — id, name, description, price, currency, categoryId
- `Category` — id, name

