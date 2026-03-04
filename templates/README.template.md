# {{NPM_PACKAGE_NAME}}@{{NPM_PACKAGE_VERSION}}

TypeScript/JavaScript client generated from OpenAPI using the native [Fetch API](https://fetch.spec.whatwg.org/).

📚 **[API Reference Documentation](https://docs.blockdaemon.com/reference/defi-account-allowance)** — Full details on all available endpoints.

## Features

- **TypeScript support** with auto-generated types
- **Dual module support** - CommonJS and ES6 modules
- **Zero dependencies** on HTTP libraries
- **Browser and Node.js** compatible
- **Tree Shaking** supported for modern bundlers

## Installation

```bash
npm install {{NPM_PACKAGE_NAME}}
```

or using Yarn:

```bash
yarn add {{NPM_PACKAGE_NAME}}
```

or using pnpm:

```bash
pnpm add {{NPM_PACKAGE_NAME}}
```

or using bun:

```bash
bun add {{NPM_PACKAGE_NAME}}
```

## Usage

### ES6 Modules

```javascript
import { AccountApi, Configuration } from "{{NPM_PACKAGE_NAME}}";

const config = new Configuration({ apiKey: "YOUR_API_KEY_HERE" }); // Replace with your actual API key
const accountApi = new AccountApi(config);
const YOUR_ADDRESS = "0xbe48eda75be2fe6af5a08749b21a6fbe49e14aa6";
const response = await accountApi.accountV1Portfolio({ address: YOUR_ADDRESS });

console.log("Native Balance (ETH):");
console.log("- Balance:", response.data.native);

response.data.evmTokens.forEach((asset) => {
  console.log(asset.name);
  console.log("- Balance:", asset.balance);
  console.log("- Symbol:", asset.symbol);
  console.log("- Address:", asset.address);
  console.log("- Decimals:", asset.decimals);
});
```

### CommonJS

```javascript
const { Configuration, AccountApi } = require("{{NPM_PACKAGE_NAME}}");

const config = new Configuration({ apiKey: "YOUR_API_KEY_HERE" }); // Replace with your actual API key
const accountApi = new AccountApi(config);
const YOUR_ADDRESS = "0xbe48eda75be2fe6af5a08749b21a6fbe49e14aa6";

accountApi.accountV1Portfolio({ address: YOUR_ADDRESS }).then((response) => {
  console.log("Native Balance (ETH):");
  console.log("- Balance:", response.data.native);

  response.data.evmTokens.forEach((asset) => {
    console.log(asset.name);
    console.log("- Balance:", asset.balance);
    console.log("- Symbol:", asset.symbol);
    console.log("- Address:", asset.address);
    console.log("- Decimals:", asset.decimals);
    console.log("- Asset Type:", asset.assetType);
  });
});
```

## Requirements

- Node.js 14+ or modern browser with Fetch API support
- For ES5 environments: Promises/A+ polyfill required
- Sign up at [app.blockdaemon.com](https://app.blockdaemon.com/signin) to create an account and generate your DeFi API key.

## Contributing

This package is auto-generated and provided as-is, contribution guidelines not included.
