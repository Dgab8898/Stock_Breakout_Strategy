
 **Breakout Strategy Project**

The objective of this project, to implement the breakout strategy, to find and remove any outliers.
Then We 'll test to see if it has the potential to be profitable using a Histogram and P-Value.
The dataset used, is the end of day from [Quotemedia](https://www.quotemedia.com).

## **Packages**

```
import sys
!{sys.executable} -m pip install -r requirements.txt
```

## **Installation**
```
import pandas as pd
import numpy as np
import helper
import project_helper
import project_tests

```


## **Load Data**

We load the data, we look at the closing prices of apple

## **Alpha research**
Started with a general observation and hypothesis, to avoid and mitigate overfitting'
We assumed we observed & research", "form hypothesis", "validate hypothesis.

## **Compute the Highs and Lows in a Window**
We used the price highs and lows as an indicator for the breakout strategy, then implemented` ```get_high_lows_lookback``` to get the maximum high price and minimum low price over a window of days

## **Compute the Highs and Lows in a Window**
Using the generated indicator of highs and lows, to create long and short signals using a breakout strategy. Implemented` ```get_long_short``` to generate the signals:
## **Filter Signals**
Implement` ```filter_signals``` to filter out repeated long or short signals within the lookahead_days.
## **Lookahead Close Prices**
To evaluate how many days to short or long the stocks, we implemented` ```get_lookahead_prices``` to get the close price days ahead in time
## **Lookahead Price Return**
We implemented` ```get_return_lookahead``` to calculate lockhead return.
## **Compute the Signal Return**
Then we computed the Signal Return
## **Test for Significance**
We plot a histogram of the signal return values.we noticed the outliers in the 10 and 20 day histograms. To better visualize the outlier

## **Kolmogorov-Smirnov Test**
We used the Kolmogorov-Smirnov Test to find the stocks that are causing these outlying returns
## **Find Outliers**
With the ks and p values calculated, we Implement the` ```find_outliers``` function to find the following:
- Symbols that pass the null hypothesis with a p-value less than` ```pvalue_threshold```.
- Symbols that with a KS value above` ```ks_threshold```.

## **Issues**
None


## **Contributing**
For major changes, please open an issue. First discuss what you would like to change. please make sure to update tests as appropriate.

**Licence**

```
Copyright (C) 2020 David Gabriel
```



## **Further Reading**

- List of code, papers, and resources for AI/deep learning/machine learning/neural networks applied to algorithmic trading.
- Machine Trading: Deploying Computer Algorithms to Conquer The Markets.
- Quantitative Trading: How to Build Your Own Algorithmic Trading Business
- https://en.wikipedia.org/wiki/Terbium
- https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.rolling.html
- https://www.learndatasci.com/tutorials/python-finance-part-3-moving-average-trading-strategy/
- https://download.ni.com/evaluation/pxi/Understanding%20FFTs%20and%20Windowing.pdf
- https://www.investopedia.com/articles/trading/09/short-term-trading.asp
- https://gist.github.com/JeromeBosman/d2a7e4ab9c7836c80e441bd3ac704d13
- https://quant.stackexchange.com/questions/40048/does-using-adjusted-closing-prices-constitute-a-lookahead-bias
- https://backtest-rookies.com/2017/06/23/tradingview-understanding-lookahead-historical-realtime-data/
- https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test
- https://docs.scipy.org/doc/scipy-0.14.0/reference/generated/scipy.stats.kstest.html#scipy-stats-kstest

