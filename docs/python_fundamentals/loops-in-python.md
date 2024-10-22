---
title: Control flow in Python 
sidebar_position: 2
---

# Control Flow statements in python

There are 8 main control flow statements that are used in python , 
### 1. If  Statement 
- to make decision based on a condition that if x conditions is true/ false , then execute a specific operation 
- to put it simply - to buy and sell if certain price is hit of a stock that you want to buy or sell
``` python
if stock_price < target_buy_price:
  place_buy_order()
```
#### 1.1 If - Else Statement
- choosing between two options, like based on analysis, buy if stock is less than x amount or else sell if the stock reaches x amount, or do this analsis using x funciton and if this doesn't happen then do this x function analysis using different funcition
- Binary trading decisions --- add more here
``` python 
if stock_price > previous_close:
  analyze_upward_trend()
else: 
  analyze_dowward_trend()
```

#### if-Elif-Else Statement
- this is just an extension of if else if the there are more than two alternative decisions to take, just on more simple syntax is added, else it is the same as if else 
- Use to choose between more than 2 alternatives
- to Choose multiple trading conditions
```python
if stock_price > upper_limit:
  sell_stock()
elif stock_price < lower_limit
```
### 2. For loops
To perform same function again and again on elements of a sequence, i.e to put it simple, to iterate a operation on a list or tuple, 
for example - this is the stock prices of a stock over the period of one week - so we have a function named 'calculate_daily_returns' which will iterate over each item in the tata_thisWeek list, and give us result, which is better than doing this operation on each item one by one
```python
tata_thisWeek = [901, 902, 900, 904, 908, 909, 911]
for stock in tata_thisWeek:
  calculate_daily_returns(stock)
```
so to put it simply - to perform the same operation on multiple items, like calculating returns for each stock in a portfolio.
### 3. While loops 
- Repeating the operation while a condition is true, When you have to run a operation on a specific stock item for certain period of time or until it has reached a price that you want it to reach and until then , you keep on iterating on it's values
- Used for continuous operations that should run as long as a condition is true, like monitoring market prices during trading hours.
- i.e stock market monitoring
```python
while market_is_open:
  monitor_price_changes()
  check_trading_signals()
  sleep(60) # wait for 1 minute
```
### 4. Break Statement 
- Exiting the current running loop when a certain condition is met, so it's like a stop- loss when price is triggered
```python
while monitoring_stock:
  current_price = get_stock_price()
  if current_price < stop_loss_price:
    execute_sell_order()
    break # exit  monitoring when the stop loss is triggered using break
```
### 5. Continue statement
- the continue statement skips a item in the loop, 
- can be used to filter  stocks if it is going under a specific price range

```python
for stock in market_stock:
  if stock.volume < minimum_value:
    continue # skip low price / volume stocks
  analyze_stock_fundamentals(stock)
```
### 6. Pass statement
- it is Used when you need syntactically valid empty code blocks or as placeholdrs for future implementation. Common in abstract
-placeholder for some future implementation or abstract classes
```python
class BasicTrader:
  def analyze_market(self):
    pass #to be implemented by specific trading strategies

class DayTrader(BasicTrader):
  def analyze_market(self):
    #actual implementation for day trading
    calculate_intraday_metrics()
```
### 7. Try -Except block
- Basically used for error handling and ensuring robust code, especially important in financial operations/programs where unexpected errors can be costly, So Try-Except just handles errors gracefully
- Some of the common Scenarios of using Try-Except block usage is:
  - Api calls to stock market
  - File operations for trading logs
  - Database Operations for storing trade data
  - Real time Network operations 
```python
def get_stock_data(symbol):
  try:
    price = api.get_current_price(symbol)
    return price
  except APIConnectError:
    log_error("API connection failed")
    return None
  except InvalidSymbolError:
    log_error(f"invalid symbol:{symbol}")
    return None
    except Exception as e:
      log_error(f"Unexpected error: {e}")
      return None
    finally:
      cleanup_connection() # always executed, whether exception occures or not
```
### 8. Switch statement 
- Pattern matching for multiple condition 
- for signal based trading
```python
match trading_signal:
  case "STRONG_BUY:
    buy_with_full_position()
  case "BUY":
    buy_with_half_position()
  case "NEUTRAL":
    hold_current_position()
  case "SELL":
    sell_current_position()
  case _: # defautl case 
    log_invalid_signal()
```
-Used when you need to match a value against multiple patterns, like different trading actions based on technical analysis signals.

