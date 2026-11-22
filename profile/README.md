# Akilibots

Configurable Python crypto trading bots. Each repository runs independently and
contains its own configuration, Docker image and regression tests.

| Bot | Behaviour | Exchange |
| --- | --- | --- |
| [akili-grid](https://github.com/akilibots/akili-grid) | Bounded moving grid | dYdX Chain |
| [akili-martingale](https://github.com/akilibots/akili-martingale) | Position averaging and weighted take profit | dYdX Chain |
| [akili-oto](https://github.com/akilibots/akili-oto) | Order-triggering-order groups and loops | dYdX Chain |
| [akili-tradingview](https://github.com/akilibots/akili-tradingview) | Authenticated TradingView webhooks | dYdX Chain |
| [akili-dca](https://github.com/akilibots/akili-dca) | Fixed-quantity interval buying or selling | dYdX Chain |
| [akili-binance-grid](https://github.com/akilibots/akili-binance-grid) | Moving two-order Spot grid | Binance Spot |

[akili-channel](https://github.com/akilibots/akili-channel) is a documentation-only
predecessor superseded by OTO.
[akilibots-strategies](https://github.com/akilibots/akilibots-strategies) is intended
for contributed configurations and currently contains no strategy files.

Docker runtimes use Python 3.15.2. dYdX bots use Chain wallets and subaccounts;
legacy v3 API credentials, STARK keys and state cannot be reused. Binance symbols
are configurable and trading fees are accounted for rather than assumed zero.
Follow the individual READMEs for testnet setup, credentials, recovery and tests.

Tests run with simulated exchange responses and networking disabled. These
repositories do not contain a hosted service, mobile app or backtesting engine.
Trading outcomes depend on configuration, execution and market conditions.

Software is supplied as is under each repository's licence.
