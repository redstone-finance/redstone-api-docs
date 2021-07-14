# Get the latest price\(s\) for a single token

{% api-method method="get" host="https://api.redstone.finance" path="/prices" %}
{% api-method-summary %}
Get price for a single token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="symbol" type="string" required=true %}
Token symbol
{% endapi-method-parameter %}

{% api-method-parameter name="provider" type="string" required=true %}
We recommend to use "redstone" provider. Learn more
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
Limit of prices
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Price successfully fetched
{% endapi-method-response-example-description %}

```text
[
  {
    "id": "11dba94e-1b1b-4c0e-ba5f-fbd6e6170cb9",
    "symbol": "TEST-SYMBOL",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 30.011,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370940870,
    "providerPublicKey": "xyz...."
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Error occurred while fetching the price
{% endapi-method-response-example-description %}

```text
Error message will be printed here
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Examples

### Get the latest price for AR token

```bash
curl "https://api.redstone.finance/prices?symbol=AR&provider=redstone&limit=1"
```

### Get the latest price for BTC token

```bash
curl "https://api.redstone.finance/prices?symbol=BTC&provider=redstone&limit=1"
```

### Get the latest 100 prices for AR token

```bash
curl "https://api.redstone.finance/prices?symbol=AR&provider=redstone&limit=100"
```

