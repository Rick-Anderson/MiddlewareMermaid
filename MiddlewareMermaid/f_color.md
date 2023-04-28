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
    Routing--->CORS
    CORS--->Authentication
    style CORS stroke: blue;
    style Authentication stroke: blue;
    Authentication--->Authorization
    style Authorization stroke: red;
    Authorization-->Authentication
    style CORS2 stroke: red;
    CORS2--->Routing
    Routing--->StaticFiles
    StaticFiles--->HttpsRedirection
    HttpsRedirection--->HSTS
    HSTS--->ExceptionHandler
    ExceptionHandler--->Response
    linkStyle 0 stroke-width:2px,fill:none,stroke:blue;
    linkStyle 1 stroke-width:2px,fill:none,stroke:blue;
    linkStyle 2 stroke-width:2px,fill:none,stroke:blue;
    linkStyle 3 stroke-width:2px,fill:none,stroke:blue;
    linkStyle 4 stroke-dasharray: 5 5, stroke-width:2px,fill:none,stroke:red;
    linkStyle 5 stroke-dasharray: 5 5, stroke-width:2px,fill:none,stroke:red;
    linkStyle 6 stroke-dasharray: 5 5, stroke-width:2px,fill:none,stroke:red;
    linkStyle 7 stroke-dasharray: 5 5, stroke-width:2px,fill:none,stroke:red;


```


