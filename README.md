# TradingStrategy

Alpha & Beta > Carry > Risk Premia

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

### Glossary

• MEAN
• MEDIAN
• MODE
• VARIANCE
• STANDARD DEVIATION
• VOLATILITY
• HISTOGRAM & NORMAL DISTRIBUTION
• SKEW & KURTIOS
• CORRELATION
• BAR CHART

