# Gold Dragon MT5

This is a forex trading expert advisor (EA) called Gold Dragon MT5, developed by Forex Robot Easy. Visit [forexroboteasy.com](https://forexroboteasy.com) for detailed reviews and trading results of this product.

## Description

Gold Dragon MT5 is a trend-based trading software designed for the MT5 platform. It trades the XAU/USD (Gold) currency pair on the H1 (1-hour) timeframe. The EA opens buy or sell trades based on the strength of the trend.

## External Parameters

- StopLoss: The stop loss value in pips (default: 100)
- TakeProfit: The take profit value in pips (default: 200)

## Expert Functions

### OnInit

This function is called during the EA initialization process. It sets up the trading account and symbol. If the FIFO (First In, First Out) rules cannot be set, it prints a failure message and returns INIT_FAILED. Otherwise, it prints a success message and returns INIT_SUCCEEDED.

### OnDeinit

This function is called when the EA is being deinitialized. It simply prints a deinitialization message.

### OnTick

This function is called on every tick. It checks if there is a new H1 candle by comparing the current hour with the previous hour. If a new candle is detected, it calculates the trend strength using the `CalculateTrendStrength()` function.

If the trend strength is positive, it opens a buy trade using the `OrderSend()` function. If the trade is opened successfully, it prints a success message. Otherwise, it prints a failure message.

If the trend strength is negative, it opens a sell trade using the `OrderSend()` function. If the trade is opened successfully, it prints a success message. Otherwise, it prints a failure message.

### CalculateTrendStrength

This function calculates the trend strength. The logic for trend strength calculation is not implemented in the code and is marked as a TODO. It returns a placeholder value of 0.

### SetFifoRules

This function sets the FIFO rules for trading. The logic for FIFO rules is not implemented in the code and is marked as a TODO. It returns a placeholder value of true, indicating success.

## Disclaimer

ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.
