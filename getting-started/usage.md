---
description: Redstone api usage
---

# Usage

First, you need to import redstone module

{% tabs %}
{% tab title="Node.js require" %}
```javascript
// Using Node.js `require()`
const redstone = require('redstone-api');
```
{% endtab %}

{% tab title="ES6 import" %}
```javascript
// Using ES6 imports
import redstone from 'redstone-api';
```
{% endtab %}
{% endtabs %}

Then you can fetch the prices with just a single line of code

```javascript
const price = await redstone.getPrice("AR");

console.log(price.value); // latest price value for AR token (in USD)
console.log(price.timestamp); // the exact timestamp of the price
```

See more examples in the documentation of the following methods:

* [getPrice](../methods/getprice.md)
* [getHistoricalPrice](../methods/gethistoricalprice.md)
* [getAllPrices](../methods/getallprices.md)

You can also check out docs for the [redstone fluent interface](../fluent-interface/build-a-query/), which makes the price fetching even simpler thanks to human readable syntax.

