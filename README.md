# krakenAPI-dca
Dollar-cost averaging Kraken crypto exchange orders using their API

This is a project to make my life easier by being able to place DCA'd orders via Kraken's API and eventually automate it with cronjobs. The Kraken API was provided by kraken.com.

Requirements:
* Python3
* kraken.com public & private API key
* adequate funding in Kraken account

Instructions: \
Download this repo, add your API keys to the appropriate files. Now you can execute commands and results will look something like this if successful.

```
0xbea@DESKTOP:~/KrakenAPI$ ./order-dca xlmusd 15
Current price per unit: 0.50175100
Volume desired: 29.89530663616016709483
{"error":[],"result":{"descr":{"order":"buy 29.89530663 XLMUSD @ market"},"txid":["A9A9A9-AAAAAA-A9A9A9"]}}
```

With the Kraken API from kraken.com, you can execute commands as follows:
```
# Kraken Rest API
#
# Usage: ./krakenapi.py method [parameters]
# Example: ./krakenapi.py Time
# Example: ./krakenapi.py OHLC pair=xbtusd interval=1440
# Example: ./krakenapi.py Balance
# Example: ./krakenapi.py OpenPositions
# Example: ./krakenapi.py AddOrder pair=xxbtzusd type=buy ordertype=market volume=0.003 leverage=5
```

To-do: \
~~1. DCA purchase function~~ \
2. Create a cronjob. \
3. More descriptive error reporting.

References:
* https://support.kraken.com/hc/en-us/articles/360025180232-Kraken-REST-API-command-line-client
* https://www.kraken.com/en-us/features/api
* https://support.kraken.com/hc/en-us/articles/205893708-Minimum-order-size-volume-for-trading
