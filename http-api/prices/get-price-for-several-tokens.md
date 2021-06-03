# Get price for several tokens

{% api-method method="get" host="https://api.redstone.finance" path="/prices" %}
{% api-method-summary %}
Get price for several tokens
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="symbols" type="string" required=true %}
Comma separated token symbols
{% endapi-method-parameter %}

{% api-method-parameter name="provider" type="string" required=true %}
Only "redstone" provider is currently supported the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The prices successfully fetched
{% endapi-method-response-example-description %}

```
{
  "AR": {
    "id": "f90a80ef-9257-4738-9c1a-8f811a2cbe43",
    "symbol": "AR",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 89.004,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370953504,
    "providerPublicKey": "xyz..."
  },
  "BTC": {
    "id": "6e249694-4a32-48bb-8bea-6b14e28406f9",
    "symbol": "BTC",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 92.912,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370953504,
    "providerPublicKey": "xyz..."
  },
  "ETH": {
    "id": "23acb6ed-ca71-418b-bfba-87cc8d6efa73",
    "symbol": "ETH",
    "provider": "I-5rWUehEv-MjdK9gFw09RxfSLQX9DIHxG614Wf8qo0",
    "value": 21.104,
    "signature": "mock+signaturQ==",
    "permawebTx": "mock-permaweb-tx",
    "version": "2",
    "source": {
      "test": 123
    },
    "timestamp": 1619370953504,
    "providerPublicKey": "xyz..."
  }
}


```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Error occurred
{% endapi-method-response-example-description %}

```
Error message will be printed here
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



