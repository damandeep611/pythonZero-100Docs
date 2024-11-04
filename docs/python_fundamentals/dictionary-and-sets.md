---
title: dictionary and set operations 
sidebar_position: 2
---

# Dictionary and set Operations 

Dictionaries stores key value pairs which are used to store structured data, for example 
``` python 
stock_prices = {
  "AAPL": 130.75,
  "GOOGL": 2220.78,
  "MSFT": 812.53
}
```

Some dictionary operations that are performed on dictionary items 
1. Accessing and modifying values in the dictionary 
``` python 
print(stock_prices["AAPL"])
```

2. Adding a new key value pair in the existing dictionary 
``` python 
stock_prices["TSLA"] = 780.90
```

3. Modifying an existing key value pair 
``` python 
stock_prices["MSFT"] = 602.72
```

4. checking if a key exits in the dictionary 
``` python 
if "AAPL" in stock_prices:
  print("Apple stock in the portfolio")
else:
  print("Stock not found")
```