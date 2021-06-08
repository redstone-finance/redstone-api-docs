---
description: Redstone api usage
---

# Usage

Firstly, you need to import redstone module

```javascript
// Using Node.js `require()`
const redstone = require('redstone-api');

// Using ES6 imports
import redstone from 'redstone-api';
```

Then you can fetch the prices with just a single line of code

```javascript
const price = await redstone.getPrice("AR");

console.log(price.value); // latest price value for AR token (in USD)
console.log(price.timestamp); // the exact timestamp of the price
```

To read more advanced examples, visit the methods documentation:

* [getPrice](../methods/getprice.md)
* [getHistoricalPrice](../methods/gethistoricalprice.md)
* [getAllPrices](../methods/getallprices.md)

You can also check out docs for the [redstone fluent interface](../fluent-interface/build-a-query.md), which makes the price fetching even simpler for most popular query use cases.

