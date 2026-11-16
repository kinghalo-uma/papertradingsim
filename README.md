# Bitcoin Paper Trader

A small browser-based Bitcoin paper trading simulator.

## Features

- Live BTC/USDT price and 24-hour percentage change from Binance public market data.
- Candlestick chart with 1m, 5m, 15m, 1h, 4h and 1d intervals.\n- Historical chart pagination: scroll left to fetch older candles in 1,000-candle batches.\n- Historical replay: choose a start date, play/pause, step candle-by-candle, and change playback speed (0.5× to 50×).\n- Replay candles are revealed progressively; future candles are hidden to avoid look-ahead bias.\n- Replay trades use a separate virtual balance from live paper trading.
- $10,000 virtual starting balance.
- Simulated market buy and sell orders with a 0.1% fee.
- Portfolio value, BTC holdings, unrealised P&L and recent trade history.
- Account state saved in the browser's local storage.

## Run locally

Open `index.html` in a modern browser, or serve the folder with any static web server.

## Publish with GitHub Pages

1. Open the repository's **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then save.
4. Wait for GitHub Pages to publish the site. The Pages URL will appear in that section.

## Notes

- Market data is read from Binance's public BTC/USDT REST and WebSocket endpoints. Historical candles are requested on demand; available depth depends on Binance's market history and API availability.
- No API key is needed; this app does not submit real orders.
- Your virtual balance and trade history stay in the current browser/device.
- A simulated fee is applied to each trade. This is a learning project, not financial advice.
