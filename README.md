# Real Time Finance : a Financial WebSocket public API

Real Time Finance is a simple websocket public API to get real-time stock prices.
The following markets are available at the moment :

- Forex
- US and European stocks companies (around 10K stocks) EURONEXT, NASDAQ, NYSE ...

# Get started

## Installing

Download rtf binaries : https://github.com/Real-time-finance/finance-websocket-API/releases
Unix, macos and windows binaries available.

## Usage example

Use market name and stock symbol to receive datas. In this example we get quotations from Netflix (nasdaq) : 
```shell
rtf add --market="NASDAQ" --stock="NFLX"
```
Another example to get quotations from Goldman Sachs (nyse) :  
```shell
rtf add --market="NYSE" --stock="GS"
```

## Output example 

```
{
  price: 386.70,
  volume: 665805,
  time: 1643359743,
  symbol: 'NFLX',
  market: 'NASDAQ'
}
```

# Available for stocks and forex

Here after you can find JSON list with symbols :

- [forex][forex]
- [companies][companies]


Further infos: https://realtimefinance.io

[forex]: ./pairs_list.json
[companies]: ./companies_list.json
