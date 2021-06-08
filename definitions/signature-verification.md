---
description: >-
  All prices saved in Redstone have a signature, therefore you can always verify
  that the price data has been submitted by the trusted provider.
---

# Signature verification

## Enable signature verification

To enable signature verification you can set `verifySignature` option to `true` in `getPrice`, `getHistoricalPrice` or `getAllPrices` methods. In case of invalid signature there will be thrown an error.

```javascript
const price = await redstone.getPrice("AR", {
  verifySignature: true,
});
console.log(price.value);
```

