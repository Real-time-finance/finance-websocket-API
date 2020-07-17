# Real Time Finance : a Financial WebSocket public API

Real Time Finance is a simple websocket public API to get real-time stock prices.
The following markets are available at the moment :

- Forex
- US and European stocks companies (around 10K stocks)

# Get started

## Installing

```
npm install ws
```

## Usage example

Use stock symbol to receive datas. In this example we use EURUSD (forex), AAPL (apple - nasdaq), MSFT (microsoft - nasdaq) and MC.PA (lvmh - cac40)
```javascript
const WebSocket = require('ws');
const ws = new WebSocket("ws://realtimefinance.io, {
  headers: {
    "API-X-KEY": "demo",
    "symbol" : "EURUSD,AAPL,MSFT,MC.PA"
  }
});

ws.on('message', function incoming(msg) {
  console.log(msg);
});
```

# Available stocks and forex

You can find here after JSON stocks list with symbol :

- [forex][forex]
- [companies][companies]

https://realtimefinance.io

[forex]: ./pairs_list.json
[companies]: ./companies_list.json
