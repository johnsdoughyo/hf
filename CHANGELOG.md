# Changelog

All notable changes to the Roboquant Universal Market Making Bot will be documented in this file.

## [1.1.0] - 2025-08-15

### Added
- **Enhanced Error Handling**: Fixed NoneType comparison errors that could cause bot crashes
- **Hyperliquid Optimization**: Specialized handling for Hyperliquid's unique requirements
- **Improved Order Management**: Better handling for exchanges that don't support `cancelAllOrders`
- **Market Data Resilience**: Fallback values for missing exchange data
- **Dynamic Spread Optimization**: Configurable spread limits for improved trade frequency

### Changed
- **Default Configuration**: Updated config.example.json with Hyperliquid-optimized settings
- **Strategy Parameters**: Reduced default gamma to 0.05 and max_spread_percent to 0.002
- **Order Size Validation**: Added minimum order size checks for Hyperliquid ($10 minimum)
- **Error Prevention**: Added `or 0` fallbacks throughout the codebase

### Fixed
- **NoneType Errors**: Prevented crashes from missing market data
- **Order Cancellation**: Fixed issues with Hyperliquid's order management
- **Precision Issues**: Resolved rounding problems that could cause order rejections
- **Market Data Handling**: Better error handling for incomplete exchange responses

### Security
- **Added .gitignore**: Prevents sensitive configuration files from being committed
- **Configuration Examples**: Safe examples without real API keys or private keys

## [1.0.0] - 2025-08-14

### Added
- **Initial Release**: Universal market making bot with Avellaneda-Stoikov strategy
- **Multi-Exchange Support**: 11+ major cryptocurrency exchanges
- **Cross-Platform**: Windows, Mac, Linux, and AWS support
- **GUI Configuration**: User-friendly setup wizard
- **Risk Management**: Built-in stop losses and position limits

### Supported Exchanges
- Binance, Bybit, OKX, KuCoin, Gate.io, MEXC, Bitget, Hyperliquid, Phemex, Huobi, Kraken

---

## How to Update

1. **Backup your current config.json** (contains your API keys)
2. **Pull the latest changes** from GitHub
3. **Update your configuration** using the new config.example.json as reference
4. **Test with small amounts** before running with full capital

## Breaking Changes

- **None**: All changes are backward compatible
- **Configuration**: Some default values have been optimized for better performance
