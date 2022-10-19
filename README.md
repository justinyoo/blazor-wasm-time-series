# Blazor WASM for Time Series Charts #

This is a Blazor WASM app displaying time series chart.


## Getting Started ##

TBD

To get OpenAPI document for the proxy API:

```bash
curl -fsSL https://aka.ms/azfunc-openapi/generate-openapi.sh \
    | bash -s -- \
        -p src/WaterConsumption.Proxy \
        -e openapi/v3.json \
        -o ./infra \
        -f openapi.json \
        -d 30
```

To generate OpenAPI proxy client:

```bash
npm install nswag -g

nswag openapi2csclient \
    /Input:"./infra/openapi.json" \
    /Output:"./src/WaterConsumption.Web/ProxyClient.cs" \
    /Namespace:"WaterConsumption.Web.Proxies" \
    /ClassName:"ProxyClient" \
    /JsonLibrary:"SystemTextJson" \
    /ServiceSchemes:"http" \
    /ServiceHost:"localhost:7071" \
    /ParameterDateTimeFormat:"u"   
```
