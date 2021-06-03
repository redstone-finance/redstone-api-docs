---
description: >-
  A cache layer is a web service, that caches prices data signed by data
  providers.
---

# Cache layer

By default, Redstone API fetches data from the Redstone cache layer. It works way faster than fetching directly from Arweave Blockchain. Even so, thanks to signature verification prices data is still trusted and secure.

### Fetching prices from Arweave Blockchain

We strongly recommend using the default fetching mechanism. But if you want to fetch data directly from Arweave you can do it by initialising a new `RedstoneApi` client and setting `useCache` option to `false`.

```javascript
const redstoneArweaveClient = new redstone.RedstoneApi({
  useCache: false,
});

const price = await redstoneArweaveClient.getPrice("AR");

console.log(price.value); // AR price value fetched directly from Arweave
```

