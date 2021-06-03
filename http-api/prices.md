# Prices

{% api-method method="get" host="https://api.redstone.finance" path="/prices" %}
{% api-method-summary %}
Get price for a single token
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="fromTIm" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="toTime" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="symbol" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="symbols" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="provider" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="fro" type="string" %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Error occurred
{% endapi-method-response-example-description %}

```text
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

