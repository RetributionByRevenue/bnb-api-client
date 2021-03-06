﻿# Binance API Client
 
## Binance API documentation
  To read more about Binance API, go to: https://binance-docs.github.io/apidocs/
  
## Note

**Official release: https://pypi.org/project/binanceAPI-abr-ver/**

***This is an unofficial Binance API wrapper written in Python. This is in no way affliated with Binance in under any circumstances. Please use at your own risk.***

**Definitely read the documentation on Binance API at [here](https://binance-docs.github.io/apidocs/) for further details and uses of this API wrapper.**

## Features

* This is a simplified wrapper version for Binance API. It is easy to learn and easy to use. This package does not cover the full documentation of Binance API as it is aimed more toward novice programmers or traders who want to make a trading bot so simplicity is key. The key and neccessary features are included for a versatile application in making trading algorithm.
* This wrapper is geared toward use of data science/visualization. Functions that return a dataframe are:
     * get_klines()
     * get_price()
     * get_24_hr_ticker()
     * get_historical_trade()
     * get_open_order()
     * get_all_order()

## How to install

**To install:**

```
pip install binanceAPI-abr-ver
```

**to import the package:**

```
#make sure you have binance.py, interval.py, and order_num.py in the same current directory as your main file
from binance.binance import BinanceClient
from binance.interval_num import Interval
from binance.order_num import Order
```

## Quickstart

```
client = BinanceClient('your-api-key', 'your-api-secret')
```
## Open an Order
```
print(client.buy('LINKUSDT', orderType=Order.MARKET ,test=False , quantity=10)) #buys $10 worth of link
print(client.sell('LINKUSDT', orderType=Order.MARKET ,test=False , quantity=10)) #sells 10 link to USD
```
For example use cases, please look into [test.py](https://github.com/mrhuytran/bnb-api-wrapper/blob/master/test.py). 

*Note that the import statements are different in test.py.*
*In test.py, we are using absolute path to import for the sake of local development.*
*However, please use the import statements specified by [How to install](https://github.com/mrhuytran/bnb-api-wrapper/blob/master/README.md#L33) if you want your code to compile.* 

## Future updates

TBA
