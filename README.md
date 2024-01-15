# Regular Winner - Trading Robot

This is the code for the Regular Winner Trading Robot developed by Forex Robot Easy Team. This robot is designed to execute trades in the Forex market based on specified input parameters.

## Input Parameters

- `FixedLotSize`: This parameter determines the fixed lot size for trading.
- `CalculationMethod`: This parameter determines the calculation method for trading volume. It can be set to `CALCULATION_FIXED_LOT`, `CALCULATION_BALANCE`, `CALCULATION_FREE_FUNDS`, or `CALCULATION_PERCENTAGE_LOSS`.
- `RiskPercentagePerTrade`: This parameter specifies the percentage of the account balance to risk per trade.
- `ProfitTarget`: This parameter sets the target profit in the account currency.
- `LossTarget`: This parameter sets the target loss in the account currency.

## Trade Variables

- `CTrade trade`: An instance of the `CTrade` class used for trade execution.
- `CArrayObj positions`: An array object to store open positions.

## Initialization

The expert advisor is initialized in the `OnInit()` function. Trade execution is enabled by setting the deviation in points and type filling.

## Trading

The trading logic is implemented in the `OnTick()` function. 

- If there are no open positions, the trading volume is calculated based on the selected calculation method. The volume is then used to open a buy position using the `trade.Buy()` function. The position is added to the positions array.
- If there are open positions, the function loops through each position and checks if it has reached the profit target or loss target. If a position reaches either target, it is closed using the `trade.PositionClose()` function and removed from the positions array.

## Resource Cleanup

The `OnDeinit()` function is responsible for cleaning up resources. In this case, the positions array is cleared.

---

Product Description:

Regular Winner - Trading Robot is a fully automated trading system developed by Forex Robot Easy Team. This robot is designed to generate consistent profits in the Forex market. It incorporates various trading strategies and risk management techniques to optimize trading performance.

Key Features:
- Fixed lot size or dynamic calculation based on account balance, free margin, or percentage loss.
- Ability to set profit and loss targets.
- Trade execution with deviation control and order filling options.
- Efficient position management to lock in profits and minimize losses.

Regular Winner - Trading Robot is suitable for both novice and experienced traders. It eliminates the need for manual trading and allows users to capitalize on market opportunities 24/5. The robot has been thoroughly tested and optimized to ensure reliable and profitable trading results.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com/forex-robot-review/regular-winner-forex-software-review-profitable-trading-at-45/](https://forexroboteasy.com/forex-robot-review/regular-winner-forex-software-review-profitable-trading-at-45/).

Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing a sample code that demonstrates how this product can work. To find the official developer of this product, please visit MQL5.
