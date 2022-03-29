# Simple Scalper Bot

Basic scalping bot for binance smart chain made by python for windows only

## How does it work?
    This program buys a token at a specified price < (**buyAt**) and will sell if you will gain x1.1 (**multiplier**) profit (buy amount + gasfee) * 1.1 
    for **BNB** if youre trading with BNB (or ETH if youre on ethereum setup) the **buyAt** is reversed 
    we will use stable coins BUSD by default as token here so if BNB price > *buyAt*  then it would by BUSD and will sell only if the price drops by 1.1 (buy amount + gasfee / 1.1)

**WARNING:** 
    * im not responsible if you choose a token that is honeypot
    * make sure you start with 0 tokens if possible or else it would automatically sell if you mess with configurations 

## Config 
```{
    "privateKey": "",
    "tokenAddress": "0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c",
    "trading": {
        "enable": false,
        "buyAt": 450,
        "buyAmount": 0.1,
        "sellMultiplier": 1.1
    },
    "network": {
        "node": "https://bsc-dataseed.binance.org",
        "router": "0x10ED43C718714eb63d5aA57B78B54704E256024E",
        "stableCoin": "0xe9e7cea3dedca5984780bafc599bd69add087d56"
    },
    "transaction": {
        "slippage": 0.3,
        "gasLimit": 300000,
        "gasPrice": 5
    },
    "shorcutKeys": {
        "buy": "F4",
        "sell": "F9",
        "approveToken": "F8",
        "toggleAutoTrade": "F1"
    },
    "refreshRate": 2
}
```

* privateKey - Your private key 
* tokenAddress - Target token address for trading (required) - Default address is BNB contract
* trading.enable - enable/disable automatic trading
* trading.buyAt - token price in USD. usage: buy token if price < buyAt, or if target token is BNB - buy BUSD if token > buyAt 
* trading.sellMultiplier = profit multiplier, if youre trading in large volume you can use smaller value must be greater than 1. eg. 1.01 for scalping
* slippage - Slippage tolerance
* gasAmount - Gas limit
* gasPrice - Gas price
* network.node = RPC endpoint default is BSC smart chain
* network.router = Dex contract address. default pancakeswap
* network.stableCoin = Stable coin address use to determine token prices, also for storing BNB profits. default is BUSD address
* shorcutKeys - as is, please check python keyboard module for the list of shorcuts
* refreshRate - how many seconds to refresh backend price monitoring. just leave it to 2 seconds


## Message
- for every sell this program sends tax for 0.0003 bnb for my address as donation<br />
- if you want to disable tax permanently or the source code email me at jpbandori25@gmail.com 
- i can make you a program for a small amount only if youre interested
- donate at 0x0000000000FC56C611BD51353BCD59C24E8a80c4