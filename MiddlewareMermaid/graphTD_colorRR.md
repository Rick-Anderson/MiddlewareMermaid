```mermaid
graph TD;
    subgraph Request
        Request
    end
    subgraph Response
        Response
    end
    Request -->|Request|ExceptionHandler
    ExceptionHandler -->HSTS
    HSTS-->Routing
    Routing-->Authenticaion
    Authenticaion--->Routing
    Routing--->HSTS
    HSTS--->ExceptionHandler
    ExceptionHandler--->|Response|Response


```
