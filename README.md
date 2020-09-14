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
const ws = new WebSocket("wss://api.realtimefinance.io", {
  rejectUnauthorized: false // use only if you are behind a firewall
});

const message = {
  event: "subscribe",
  data: ['EURUSD','GBPUSD','AAPL','MSFT']
};
ws.on("open", function open() {
  ws.send(JSON.stringify(message));
});

ws.on("message", function incoming(data) {
  console.log(data);
});
```

# Available for stocks and forex

Here after you can find JSON list with symbols :

- [forex][forex]
- [companies][companies]


Further infos: https://realtimefinance.io

[forex]: ./pairs_list.json
[companies]: ./companies_list.json
