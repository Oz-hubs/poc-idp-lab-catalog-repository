# shop-catalog-graphql-api

GraphQL API exposed by `shop-catalog-graphql-service`.

- **Type:** graphql
- **Provider:** `shop-catalog-graphql-service`

## Query surface

- `product(id: ID!)`
- `products(category: String, limit: Int = 20)`
- `categories`
- `stock(productId: ID!)`

## Schema source

- Source file: [`schema.graphql`](../schema.graphql)
- In Backstage: open `shop-catalog-graphql-api` and switch to the **Definition** tab.
