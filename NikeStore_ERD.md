# Ilya-xp.github.io


```mermaid
erDiagram
    PRODUCT ||--o{ SALE : "sells"
    CUSTOMER ||--o{ SALE : "buys"
    PRODUCT ||--o{ INVENTORY : "has"
    
    **PRODUCT** {
        string product_id PK
        string model_name
        float price
    }
    
    **CUSTOMER** {
        string customer_id PK
        string name
        string email
    }
    
    **SALE** {
        string sale_id PK
        string product_id FK
        string customer_id FK
        date date
        int quantity
        float total_price
    }
    
    **INVENTORY** {
        string inventory_id PK
        string product_id FK
        int quantity_available
    }