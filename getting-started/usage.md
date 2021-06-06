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

* [getPrice](https://docs.redstone.finance/methods/getprice)
* [getHistoricalPrice](https://docs.redstone.finance/methods/gethistoricalprice)
* [getAllPrices](https://docs.redstone.finance/methods/getallprices)

You can also check out docs for the [redstone fluent interface](https://api.docs.redstone.finance/fluent-interface/build-a-query), which makes the price fetching even simpler for most popular query use cases.

