---
description: query method is used to initialise a redstone query
---

# query

## Simple example

```javascript
const price = await redstone.query()
  .symbol("AR")
  .latest()
  .exec();

console.log(price.value); // latest price value for AR token (in USD)
console.log(price.timestamp); // the exact timestamp of the price
```

To learn more, visit [the Redstone Query page](../fluent-interface/build-a-query/)

{% page-ref page="../fluent-interface/build-a-query/" %}

