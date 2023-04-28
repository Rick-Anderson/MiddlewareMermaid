```mermaid
graph TD;
    subgraph Request-Response
        Request((Request))
        Response((Response))
    end
    Request--->ExceptionHandler
    ExceptionHandler--->HSTS
    HSTS--->HttpsRedirection
    HttpsRedirection--->StaticFiles
    StaticFiles--->Routing
    Routing--->Authentication
    Authentication--->Routing
    Routing--->CORS
    CORS--->Authorization
    Authorization--->Custom1
    Custom1--->endpoint
    endpoint--->Authentication
    Authentication--->HttpsRedirection
    HttpsRedirection--->HSTS
    HSTS--->ExceptionHandler
    ExceptionHandler--->Response
```
