# Simple BSC Trading Bot

This is just for testing purposes and my first python project compiled for windows os. Im currently working on strategies and it will take a while since im just a newbie. 

## Features
* auto trade bot if the price of token reach a certain amount it will automatically buy / sell
* snipe new token for liquidity
* snipe specific token for liquidity
* honeypot detection and bypass trading delays
* use only USDT (bep20) for trading
* disable auto trades, but can buy / sell manually using shorcut keys
* can assign shorcut keys in config
* shows how many USDT you lose and gain after selling token
* auto sell token if no trades found within x seconds (configurable in config.json)

## Config 
```json
{
    "privateKey": "",
    "tokenAddress": "0x9573c88ae3e37508f87649f87c4dd5373c9f31e0",
    "network": {
        "symbol": "BNB",
        "node": "https://bsc-dataseed3.ninicoin.io"
    },
    "transaction": {
        "slippage": 1,
        "gasLimit": 350000,
        "gasPrice": 10
    },
    "autoTrade": false,
    "trading": {
        "buyAmount": 10,
        "sellMultiplier": 1,
        "buyingPrice": 1,
        "sellingPrice": 2,
        "stopLoss": 0.2
    },
    "sniping": {
        "checkHoneypot": true,
        "honeypotTimeout": 200,
        "requireVerified": true,
        "minimumLiquidity": 50,
        "sellWaitTime": 60,
        "blacklistedWords": ["test", "floki"]
    },
    "api":{
        "explorer": ""
    },
    "shorcutKeys": {
        "buy": "F1",
        "sell": "F9",
        "toggleAutoTrade": "Enter",
        "approveUSDT": "F4",
        "approveToken": "F5"
    },
    "router": {
        "routerAddress": "0x10ED43C718714eb63d5aA57B78B54704E256024E",
        "wrappedAddress": "0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c",
        "USDTAddress": "0x55d398326f99059ff775485246999027b3197955"
    }
}
```

* walletPrivateKey - Your private key 
* tokenAddress - Target token address for trading (required)
* network > symbol - BNB or ETH
* network > node - RPC Node supported http and wss
* slippage - Slippage tolerance
* gasAmount - Gas limit
* gasPrice - Gas price
* autoTrade - toggle auto-trading mode
* trading > buyAmount - how much USDT to spend every trades (0 - to spend all)
* trading > sellMultiplier - sell token if you reach certain amount of USDT 
* trading buyingPrice and sellingPrice - buy / sell price if token price reach around this value
* trading > stopLoss only works in trading option, auto sell token when price goes below 20% (default 0.2)
* sniping > checkHoneypot - check if token is honeypot
* sniping > honeypotTimeout - how much time to wait for token to be tradable before going back to sniping
* sniping > requireVerified - check if source code is verified in explorer (bscscan)
* sniping > sellWaitTime - how many seconds to wait if no trades found 
* sniping > blacklistedWords - blacklist word in token name or symbol (default: ["test", "floki"])
* api > explorer - your bscscan api 
* shorcutKeys - as is, please check python keyboard module for the list of shorcuts
* router > routerAddress - pancakeswap router address
* router > wrappedAddress - WBNB or WETH address if youre on BSC use WBNB contract address
* router > USDTAddress - USDT contract address, Bep20 


## Message
- This is only test project and is 100% safe, always try to make separate wallet address for this kind of projects thank you<br />
- This program consumes a little amount of 5% tax USDT if you gain morethan 100 USDT
If you want the source code email me :) <br/><br/>
I hope this works and help others Thank you very much. email me at jpbandori25@gmail.com 