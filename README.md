# Key Levels Indicator

This repository contains a TradingView Pine Script indicator called "Key Levels." This script is designed to identify and plot significant key levels on a price chart, assisting traders and technical analysts in making informed decisions. The script supports various trading symbols, including "EURUSD," "AUDCHF," "NZDCAD," and "GBPJPY," each with specific rounding and increment rules.

## Overview

The "Key Levels" indicator is a valuable tool for identifying support and resistance levels in different financial markets. It offers a flexible and adaptable approach, allowing traders to visualize key levels tailored to their chosen trading symbol.

## Indicator Features

### Variables

- `symbol`: Stores the trading symbol/ticker currently being viewed.

- `base_level_plotted`: A boolean flag that tracks whether the base key level has been plotted yet.

- `current_price`: Represents the closing price of the current bar.

- `base_key_level`: Calculates the base key level based on the trading symbol. The key levels are rounded values derived from the symbol's price.

- `above_base_key_level_increments` and `below_base_key_level_increments`: Initialize with the same value as `base_key_level` and are used to adjust key levels above and below.

- `box_increment`: Specifies the increment value used for drawing boxes around key levels.

### Logic

1. The script starts by specifying Pine Script version 5 and creates an indicator titled "Key Levels," which overlays the price chart.

2. It initializes several variables for tracking and calculations, ensuring compatibility with various trading symbols.

3. The script enters a loop that runs 10 times, with the loop variable `iteration` ranging from 1 to 10. Within this loop:

   - It checks if `base_level_plotted` is `false`. If true, it plots a box and a dashed line around the base key level to mark it on the chart. It also sets `base_level_plotted` to `true`.

   - If `base_level_plotted` is `true`, it plots boxes and dashed lines for key levels above and below the base key level, with the number of boxes and lines determined by the current iteration.

4. Inside the loop, the script adjusts the `above_base_key_level_increments` and `below_base_key_level_increments` variables based on the trading symbol. For certain symbols, such as "EURUSD," "AUDCHF," and "NZDCAD," increments are set to 0.01, while for "GBPJPY," increments are 5.

## Usage

This indicator can be added to your TradingView charts to visualize key levels for your chosen trading symbol. It does not provide trading signals or specific strategy logic but focuses on helping traders identify important price levels.

Feel free to customize and adapt the indicator to your trading strategy and preferences by modifying variables, adjusting increments, or adding additional functionality.

## License

This script is subject to the terms of the Mozilla Public License 2.0. For more information, please refer to the [Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/).

## Author

This script was authored by [KeidenIsKayden](https://github.com/KeidenIsKayden).

---

**Disclaimer:** This script is provided for educational purposes and does not constitute financial advice. Use it responsibly and at your own risk when trading or investing.
