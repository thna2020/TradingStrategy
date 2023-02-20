# TradingStrategy

Alpha & Beta > Carry > Risk Premia

*Steps*

Return, Cummulative Return, Distribution, Volatility, Correlation....

Backtesting

## Stock Analysis

### Excel Formula

> match closing price with dividend payout using date column

```
= IFERROR(VLOOKUP(A5,'I. Dividend Info'!$A$5:$B$24,2,FALSE),0)
```

> high within a given time period i.e., year

```
=MAX(IF(('I. Stock Info'!A:A<=DATE(A5,12,31))*('I. Stock Info'!A:A>=DATE(A5,1,1)),'I. Stock Info'!C:C,""))
```

> low within a given time period i.e., year

```
=MIN(IF(('I. Stock Info'!A:A<=DATE(A5,12,31))*('I. Stock Info'!A:A>=DATE(A5,1,1)),'I. Stock Info'!D:D,""))
```

> average closing price within a given time period i.e., year

```
=AVERAGE(IF(('I. Stock Info'!A:A<=DATE(A5,12,31))*('I. Stock Info'!A:A>=DATE(A5,1,1)),'I. Stock Info'!E:E,""))
```

> yearly closing price

```
=INDEX('I. Stock Info'!E:E,MATCH(LARGE(IF(('I. Stock Info'!A:A<=DATE(A5,12,31))*('I. Stock Info'!A:A>=DATE(A5,1,1)),'I. Stock Info'!A:A,""),1),'I. Stock Info'!A:A,0))
```

> average dividend within a given time period i.e., year

```
=AVERAGE(IF(('I. Dividend Info'!A:A<=DATE(A5,12,31))*('I. Dividend Info'!A:A>=DATE(A5,1,1)),'I. Dividend Info'!B:B,""))
```

> average volume within a given time period i.e., year

```
=AVERAGE(IF(('I. Stock Info'!A:A<=DATE(A5,12,31))*('I. Stock Info'!A:A>=DATE(A5,1,1)),'I. Stock Info'!F:F,""))
```

### Commmentary Template

- Apple's stock price has been increasing since 2017 albeit at a varied pace. It has increased from $28.95 to $178.2 since Jan'2017 representing a 516% increase over the 5-year period.
- As can be been by the range in each year (i.e. the difference between the maximum and the minimum price), the highest volatility has been during 2020. This could be directly attributed to March'20 broadscale equity market sell-off driven by the Covid-19 pandemic.
- Both Average Closing Price and Yearly Closing Price have been increasing throughout the period.
- Average dividends have constantly increased despite volatility in the share prices. Average annual dividend payments have increased from $0.15 to $0.22 representing c.47% increase since 2017. This indicates that Apple has enough reserves to pay out regular dividends, and there is no strong correlation between the share price and dividend payments.
- Both dividends and share prices have been increasing since 2017.
- The average trading volume over the five periods has been volatile but there isn't any conclusive pattern.

## Concepts

### Instruments

> Stocks

- Large cap
- Small cap

> ETFs

- Equity Index
- Bond Index
- Commodities
- Alternatives

> FX / CFD

> Cryptocurrencies

> Futures

> Options

### Risk Premia

> Equity

> Bond

> Volatility

> Illiquidity

### Factor Styles

> Short Term MR (short-term momentum returns)

> Momentum

> Carry

> Value

> Low Volatility

### Other Inefficiencies

> Seasonality

- Price
- Volatility

> Cointegration
> Event under / overreaction

### Strategies

> Beta / Factor

- Diversified "risk premia"
- Momo / Trend following
- Mean Reversion
- Carry trading
- Volatility Selling
- Value investing
- Seasonality trades
- "Betting against beta"

> Alpha
- Pairs trading / Stat arb
- Events trading
- Options relative value
- Small cap "pump and dump"
- Scalping / skew trades
- Market making

### Other Ideas

> P2P Lending

> Real Estate

> Betting & prediction markets

## US Indices

> Dow. 

> S&P 500. 

> Nasdaq. 

> Russell 2000. 

> CBOE Volatility Index.

## S&P 500 Sectors

> Consumer Staples. 

> Utilities. 

> Financials. 

> Telecom. 

> Healthcare. 

> Industrials. 

> Information Technology. 

> Materials. 

> Energy%. 

> Consumer Discretionary.

## World Indices

> London

> France

> Germany

> Japan

> China

> Hong Kong

> India

## Commodities and Bonds

> Crude Oil WTI. 

> Gold. 

> Natural Gas. 

> Ten-Year Bond Yield.

## Forex and Cryptos

> EUR/USD. 

> USD/JPY. 

> GBP/USD. 

> Bitcoin. 

## References


https://alphaarchitect.com/2015/12/quantitative-momentum-investing-philosophy/

https://quantocracy.com/

https://www.quantrocket.com/blog/hedging-long-term-risk-intraday-strategy/

https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2440866

https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3460965

https://towardsdatascience.com/an-even-easier-guide-to-getting-stock-data-with-python-1a109df6b593

https://www.wallstreetoasis.com/resources/careers/jobs/sales-and-trading

https://www.wallstreetoasis.com/resources/skills/accounting/profit-and-loss-pnl

https://www.codingfinance.com/post/2018-04-10-cumulative-portfolio-returns-py/
