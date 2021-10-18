# Simple BSC Trading Bot

This is just for testing purposes and my first python project compiled for windows os. Im currently working on strategies and it will take a while since im just a newbie. 

## Features
* Monitor realtime price
* Trigger buy / sell manually
* Buy and Sell if certain price is reached
* Listen to token address for liquidity and auto buy

## Config 
```json
{
   "walletAddress": "",
   "walletPrivateKey": "",
   "pairAddress": "0xe9e7cea3dedca5984780bafc599bd69add087d56",
   "tokenAddress": "",
   "bscNode": "wss://bsc-ws-node.nariox.org:443",
   "slippage": 1,
   "gasAmount": 350000,
   "gasPrice": 7,
   "buyAmount": 0,
   "snipeTokenMode": false,
   "monitorOnly": true,
   "sellMultiplier": 1,
   "buyWhenPriceAt": 0.02,
   "sellWhenPriceAt": 5
}
```

* walletAddress - Your BSC wallet address 
* walletPrivateKey - Your private key 
* pairAddress - Contract address of coin to use when trading, default: is BUSD since its more stable than BNB make sure you have enough BUSD balance and BNB for gas fees 
* tokenAddress - Target token address for trading
* bscNode - BSC Node Server leave blank if you dont have one
* slippage - Slippage tolerance
* gasAmount - Max gas amount
* gasPrice - Gas price
* buyAmount - How much (pair address token balance to trade) eg. how much BUSD to trade to target token. Note: set this to 0 to enable buying using all your token 
* snipeTokenMode - Experimental! use this to listen to upcoming launch in pancakeswap, triggers when liquidity is added 
* monitorOnly - Set this to true first to know how this app works, this disables auto buy and sell
* sellMultiplier - Automaticalyl sell token when price multiplier reach, this only work if the value is greater than 1
* buyWhenPriceAt - Buy token when token price reach below this value
* sellWhenPriceAt - Sell token when reached target value, disables when sellMultiplier is enabled

```
# Hotkeys
F1 - Manual Buy of Token
F2 - Manual Sell of Token
F9 - Manual Approve of token
```

## Message
This is only test project and i wont be selling this. This is 100% safe, always try to make separate wallet address for this kind of projects thank you<br />
You can donate small amount of bnb: 0x20002C0055A0e0000D500f020404BAC08e802085 </b> <br />
If you want the source tho im not confident in my code :) 
