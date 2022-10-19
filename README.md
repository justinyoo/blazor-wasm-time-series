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
