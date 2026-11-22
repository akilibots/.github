<p align="center"><img src="https://raw.githubusercontent.com/akilibots/.github/main/assets/akilibots-icon.svg" width="144" alt="Akilibots"></p>

# Welcome to Akilibots! 🤖

[![Python 3.15.2](https://img.shields.io/badge/Python-3.15.2-6966FF?logo=python&logoColor=white)](https://www.python.org/downloads/)
[![Telegram](https://img.shields.io/badge/Telegram-community-6966FF?logo=telegram&logoColor=white)](https://t.me/+9F0CZj8emLc2YTY0)

> **Updated 22 November 2026:** the bots are refreshed for **Python 3.15.2**, **dYdX Chain** and the current **Binance Spot SDK**. All six executable bots have Docker regression tests and CI.

Jambo! and welcome! **Akilibots** is a family of configurable, non-opinionated
crypto trading bots. The word **akili** means brain or mind in Swahili.

This project grew out of frustration with commercial bots that always seemed to
miss that one little tweak. Here, you choose the strategy, quantities and order
sequence. There is room to experiment, and the source is here to understand and
change. 🤖

## Meet the bots

| Bot | What it does | Exchange |
| --- | --- | --- |
| 🔥 [akili-grid](https://github.com/akilibots/akili-grid) | Keeps buys and sells around a bounded moving grid | dYdX Chain |
| 📈 [akili-martingale](https://github.com/akilibots/akili-martingale) | Averages into a position and adjusts weighted take profit | dYdX Chain |
| ⛹️ [akili-oto](https://github.com/akilibots/akili-oto) | Runs order groups, transitions and repeating loops | dYdX Chain |
| 📺 [akili-tradingview](https://github.com/akilibots/akili-tradingview) | Turns authenticated TradingView alerts into queued orders | dYdX Chain |
| ⌚ [akili-dca](https://github.com/akilibots/akili-dca) | Buys or sells a fixed quantity at your chosen interval | dYdX Chain |
| ♨️ [akili-binance-grid](https://github.com/akilibots/akili-binance-grid) | Keeps a moving buy and sell on a configurable Spot market | Binance Spot |

[akili-channel](https://github.com/akilibots/akili-channel) is the original channel
concept, now covered by OTO. [akilibots-strategies](https://github.com/akilibots/akilibots-strategies)
is ready for contributed configurations; no strategy files are included there yet.

## What is new

- Python **3.15.2** Docker images and updated exchange dependencies.
- dYdX **Chain** wallets and subaccounts in place of the retired v3 integration.
- Persistent order IDs and recovery checks to prevent duplicate submissions.
- Quantity-weighted averaging and actual fill-and-fee accounting where profit is reported.
- A durable TradingView queue with authenticated requests and job status.
- **108 passing offline tests** across the six bot suites, plus GitHub CI.

## Get started

1. Pick a bot above and open its README.
2. Clone it, copy `.env.example` to `.env`, and configure its sample for testnet.
3. Review the market, prices and quantities, then run the Docker tests.
4. Start it with `docker compose up --build -d` and follow its logs.

Each bot runs independently. Keep separate data folders and subaccounts for
separate strategies. dYdX v3 API keys, STARK keys and old state cannot be reused
with the Chain bots. The individual READMEs explain credentials, recovery,
cancellation and the cases that stop for reconciliation.

Tests use simulated exchange responses with networking disabled. They verify
program behaviour, not live execution or profitable trading.

## The usual bit

This software is for educational purposes only. Do not risk money you are afraid
to lose. **USE THE SOFTWARE AT YOUR OWN RISK. THE AUTHORS AND ALL AFFILIATES ASSUME
NO RESPONSIBILITY FOR YOUR TRADING RESULTS.**

Come say jambo in [Telegram](https://t.me/+9F0CZj8emLc2YTY0).
