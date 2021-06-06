---
description: >-
  All prices saved in Redstone have a signature, thanks to which you always can
  verify if the price data has been submitted by the trusted provider.
---

# Signature verification

## Enable signature verification

To enable signature verification you can set `verifySignature` option to `true` in `getPrice`, `getHistoricalPrice` or `getAllPrices` methods. If signature is invalid - error will be thrown.

```javascript
const price = await redstone.getPrice("AR", {
  verifySignature: true,
});
console.log(price.value);
```

