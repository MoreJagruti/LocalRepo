graph LR
    A[User] --> B(Dashboard.py);
    B --> C{CRUD Operations};
    C -- Employee --> D[Employee.py];
    C -- Supplier --> E[Supplier.py];
    C -- Product --> F[Product.py];
    C -- Category --> G[Category.py];
    C -- Sales --> H[Sales.py];
    B --> I[Billing.py];
    D --> J(SQLite3 Database);
    E --> J;
    F --> J;
    G --> J;
    H --> J;
    I --> J;
    K[create_db.py] --> J;
    B --> L[OS Module (File System)];
    I --> L;
    B --> M[PIL (Image Handling)];
    B --> N[Datetime Module];
    subgraph "Python Scripts"
        B; D; E; F; G; H; I; K;
    end
    subgraph "Python Modules"
        J; L; M; N;
    end
