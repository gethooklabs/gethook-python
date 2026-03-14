# gethook — Python SDK

Python client for the [GetHook](https://gethook.io) Webhook Reliability Gateway API.

## Installation

```bash
pip install gethook
```

## Usage

```python
from gethook import ApiClient, Configuration
from gethook.api import SourcesApi, DestinationsApi, RoutesApi, EventsApi

config = Configuration(
    host="https://api.gethook.io",
    api_key={"ApiKeyAuth": "hk_your_api_key"},
)

with ApiClient(config) as client:
    sources = SourcesApi(client).list_sources()
    print(sources)
```

## Documentation

Full API reference: https://docs.gethook.io/api-reference.html

## Development

This SDK is auto-generated from the OpenAPI spec via `make sync` in the main [gethook](https://github.com/gethook/gethook) repo.
