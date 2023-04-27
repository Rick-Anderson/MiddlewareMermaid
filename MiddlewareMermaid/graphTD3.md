```mermaid
graph TD;
    A[Exception Handling] <--> B[HTTPS Redirection];
    B --> C[Static Files];
    C --> D[Routing];
    D --> E[Authentication];
    E --> F[CORS];
    F --> G[Custom Middleware];
    
    B --> C;
    C --> D;
    D --> E;
    E --> F;
    F --> G;
```