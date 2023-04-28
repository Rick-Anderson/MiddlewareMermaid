```mermaid
graph TD;
    subgraph Request-Response
        Request((Request))
        Response((Response))
    end
    Request--->ExceptionHandler
    ExceptionHandler--->HSTS
    HSTS--->HttpsRedirection1
    HttpsRedirection1--->Routing
    Routing--->Authentication
    Authentication--->Routing
    Routing--->HttpsRedirection2
    HttpsRedirection2--->HSTS
    HSTS--->ExceptionHandler
    ExceptionHandler--->Response

    HSTS--xRouting
    Routing--xHSTS
    Authentication--xAuthorization
    Authorization--xCustomMiddleware1
    CustomMiddleware1--xEndpoint

```
