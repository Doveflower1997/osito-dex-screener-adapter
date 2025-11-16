# DEX Screener Adapter for Osito Protocol on Berachain 🌐🔗

![GitHub release](https://img.shields.io/github/release/Doveflower1997/osito-dex-screener-adapter.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Issues](https://img.shields.io/github/issues/Doveflower1997/osito-dex-screener-adapter.svg)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Overview

The **DEX Screener Adapter for Osito Protocol** is designed to facilitate tracking of Osito swap data on Berachain. This adapter serves as a bridge, enabling users to seamlessly access and analyze decentralized exchange data. With this tool, developers and users can monitor transactions, track liquidity, and gain insights into market trends.

## Features

- **Real-time Data Tracking**: Access live swap data from the Osito protocol.
- **Easy Integration**: Designed for simple integration with existing applications.
- **Lightweight**: Built with performance in mind, ensuring quick responses.
- **TypeScript Support**: Fully written in TypeScript for better type safety.
- **Comprehensive API**: Offers a wide range of endpoints for various data needs.

## Installation

To install the DEX Screener Adapter, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Doveflower1997/osito-dex-screener-adapter.git
   ```

2. Navigate to the project directory:
   ```bash
   cd osito-dex-screener-adapter
   ```

3. Install the dependencies:
   ```bash
   npm install
   ```

4. Build the project:
   ```bash
   npm run build
   ```

## Usage

To use the DEX Screener Adapter, you need to set up your API keys and configure the environment. Here’s a simple example of how to get started:

1. Create a configuration file (e.g., `config.json`):
   ```json
   {
     "apiKey": "YOUR_API_KEY",
     "baseUrl": "https://api.berachain.com"
   }
   ```

2. Import the adapter in your application:
   ```typescript
   import { DexScreenerAdapter } from './src/DexScreenerAdapter';

   const adapter = new DexScreenerAdapter('YOUR_API_KEY');

   adapter.getSwapData()
     .then(data => {
       console.log(data);
     })
     .catch(error => {
       console.error('Error fetching swap data:', error);
     });
   ```

3. Run your application:
   ```bash
   node yourApp.js
   ```

## API Reference

### Get Swap Data

**Endpoint**: `/api/swap-data`

**Method**: `GET`

**Description**: Fetches the latest swap data for the Osito protocol.

**Parameters**:
- `limit`: (optional) Number of records to return.
- `offset`: (optional) Number of records to skip.

**Example**:
```typescript
adapter.getSwapData({ limit: 10 })
  .then(data => {
    console.log(data);
  });
```

### Get Liquidity Data

**Endpoint**: `/api/liquidity-data`

**Method**: `GET`

**Description**: Retrieves liquidity information for the Osito protocol.

**Parameters**:
- `pair`: (required) The trading pair to query.

**Example**:
```typescript
adapter.getLiquidityData({ pair: 'OSITO-BTC' })
  .then(data => {
    console.log(data);
  });
```

## Contributing

We welcome contributions to the DEX Screener Adapter. To get involved:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a pull request.

Please ensure that your code adheres to our coding standards and that you include tests for new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For the latest releases, visit the [Releases section](https://github.com/Doveflower1997/osito-dex-screener-adapter/releases). Download the latest version and execute it to start using the DEX Screener Adapter.

For more detailed information, please check the [Releases section](https://github.com/Doveflower1997/osito-dex-screener-adapter/releases) for updates and version history.

## Acknowledgments

- Special thanks to the Osito protocol team for their support.
- Thanks to the Berachain community for their valuable feedback.

![Blockchain](https://example.com/blockchain-image.png)
![DeFi](https://example.com/defi-image.png)

## Contact

For questions or support, please reach out via GitHub issues or contact the maintainers directly.