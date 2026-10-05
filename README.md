## Assignment

Assignment 2: Design Database ERD.

| | |
|---|---|
| **Student** | (Muhammad Rizky) |
| **NPM** | (2410010226) |
| **Class** | (5C) |
| **Phase** | P02: Design Database ERD |
| **Status** | Done |
| **Fork / branch** | https://github.com/rizkymhmd06/Tugas-1-PBO-2 / feature/design-database |

## What was done

| Job | Description | Status |
|---|---|---|
| J1 | Add Name and NPM to README | Done |
| J2 | Add Design Database ERD | Done |

## Design Database ERD

```mermaid
erDiagram
    USERS ||--o{ ORDERS : membuat
    ORDERS ||--|{ ORDER_ITEMS : berisi
    PRODUCTS ||--o{ ORDER_ITEMS : dipesan

    USERS {
        bigint id PK
        string name
        string email
        string password
    }
    ORDERS {
        bigint id PK
        bigint user_id FK
        date order_date
        decimal total
    }
    PRODUCTS {
        bigint id PK
        string name
        decimal price
        int stock
    }
    ORDER_ITEMS {
        bigint id PK
        bigint order_id FK
        bigint product_id FK
        int quantity
    }
```