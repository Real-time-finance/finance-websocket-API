# Real Time Finance : a Financial WebSocket public API

Real Time Finance is a simple websocket public API to get real-time stock prices.
The following markets are available at the moment :

- Forex
- US and European stocks companies (around 10K stocks)

# Installing

```
npm install ws
```

# Usage example

```javascript
const WebSocket = require('ws');
const ws = new WebSocket("ws://realtimefinance.io, {
  headers: {
    "api_key": "demo",
    "symbol" : "AUDUSD", "AAPL", "^DJI"
  }
});

ws.on('message', function incoming(msg) {
  console.log(msg);
});
```

# JSON stocks list

You can find here after JSON stocks list with symbol :

- [forex][forex]
- [companies][companies]

  https:/realtimefinance.io

[forex]: ./pairs_list.json
[companies]: ./companies_list.json
