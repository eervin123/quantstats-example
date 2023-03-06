# Quantstats Example

## Table of Contents

- [Quantstats Example](#quantstats-example)
  - [Table of Contents](#table-of-contents)
  - [About ](#about-)
  - [Getting Started ](#getting-started-)
    - [Prerequisites](#prerequisites)

## About <a name = "about"></a>

Simple example highlighting the quantstats library. Note, currently the quantstats package can't handle timezone aware indexes so you need to remove the tz aware bit.

```
# fetch the daily returns for a stock and remove the timezone info

stock = qs.utils.download_returns('GOOG')
stock.index = stock.index.tz_localize(None) # remove timezone info this is a bug in quantstats

# create a benchmark
bench = qs.utils.download_returns('SPY')
bench.index = bench.index.tz_localize(None) 
```

## Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 
`pip install quantstats`
or 
`conda install -c ranaroussi quantstats`

### Prerequisites

- Python >= 3.5+
- pandas (tested to work with >=0.24.0)
- numpy >= 1.15.0
- scipy >= 1.2.0
- matplotlib >= 3.0.0
- seaborn >= 0.9.0
- tabulate >= 0.8.0
- yfinance >= 0.1.38
- plotly >= 3.4.1 (optional, for using plots.to_plotly())
