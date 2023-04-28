```mermaid
graph TD;
    Request-->|Request|ExceptionHandler
    ExceptionHandler-->HSTS
    HSTS-->Routing
    Routing-->Authentication
    Authentication--->Routing2
    Routing2--->HSTS2
    HSTS2--->ExceptionHandler2
    ExceptionHandler2--->|Response|Response
    subgraph Request
        Request[Request]
    end
    subgraph Response
        Response[Response]
    end

```
