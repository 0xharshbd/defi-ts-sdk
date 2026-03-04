# Blockdaemon DeFi API TypeScript SDK Generator

This repository contains the tooling to generate and build the **@blockdaemon/defi-api-sdk** TypeScript client from the Blockdaemon DeFi API OpenAPI specification.

The Blockdaemon DeFi API provides a single interface to a multitude of DeFi projects and blockchains. The generated SDK offers a type-safe client for interacting with this API.

## Prerequisites

- **Node.js** >= 14.0.0
- **npm** >= 6.0.0
- **Docker** (for OpenAPI code generation)

## Building the SDK

```bash
npm install
npm run build
```

The build process:

1. Generates TypeScript client code from `swagger/openapi.yml` using OpenAPI Generator
2. Configures the package for npm publishing
3. Compiles to CommonJS and ESM with type definitions

Output is written to the `dist/` directory.

## Version

To build with a specific version:

```bash
VERSION=1.2.3 npm run build
```

## Generated Package

The build produces `@blockdaemon/defi-api-sdk`, which can be installed from npm:

```bash
npm install @blockdaemon/defi-api-sdk --save
```

## Documentation

- [Blockdaemon DeFi API Documentation](https://www.blockdaemon.com/api/defi)
- [Supported Chains](https://docs.blockdaemon.com/docs/defi-api-supported-protocols#supported-chains)

## License

MIT
