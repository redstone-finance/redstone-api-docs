# Get historical price\(s\) for a single token

* [List of all supported tokens](https://github.com/redstone-finance/redstone-api/blob/main/docs/ALL_SUPPORTED_TOKENS.md)
* [Available providers](../../definitions/provider.md)

{% api-method method="get" host="https://api.redstone.finance" path="/prices" %}
{% api-method-summary %}
Get several prices for a single token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
Limit of prices
{% endapi-method-parameter %}

{% api-method-parameter name="symbol" type="string" required=true %}
Token symbol
{% endapi-method-parameter %}

{% api-method-parameter name="provider" type="string" required=true %}
Only "redstone" provider is currently supported
{% endapi-method-parameter %}

{% api-method-parameter name="fromTimestamp" type="string" required=false %}
Minimal timestamp in milliseconds
{% endapi-method-parameter %}

{% api-method-parameter name="toTimestamp" type="string" required=true %}
Maximum timestamp in milliseconds
{% endapi-method-parameter %}

{% api-method-parameter name="interval" type="number" %}
Interval in milliseconds
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Token prices successfully retrieved.
{% endapi-method-response-example-description %}

```text
[
  {
    "id": "aba0cf4d-cc26-446f-9096-37fedfab6854",
    "symbol": "TEST-SYMBOL",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 97.152,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370944944,
    "minutes": 16,
    "providerPublicKey": "xyz..."
  },
  {
    "id": "eed207bd-5ff5-4c30-b63b-4523d40bfa6e",
    "symbol": "TEST-SYMBOL",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 80.673,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370945945,
    "minutes": 16,
    "providerPublicKey": "xyz..."
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Error occurred while fetching the prices
{% endapi-method-response-example-description %}

```text
Error message will be printed here
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Examples

### Get  single historical price for ETH token at specified time

Example for timestamp: `1621108871711` `(2021-05-15T20:01:11.711Z)`

```bash
curl "https://api.redstone.finance/prices?symbol=AR&provider=redstone&toTimestamp=1621108871711&limit=1"
```

### Get the historical prices for AR token

```bash
curl "https://api.redstone.finance/prices?symbol=AR&provider=redstone&fromTimestamp=1619546099466&toTimestamp=1619547041149&interval=1"
```

