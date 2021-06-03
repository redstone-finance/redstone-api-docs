---
description: Simple example of redstone-api usage
---

# Usage

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

