# Analyzing Data: Tesla Stock and Revenue

Extracts Tesla's historical stock price and quarterly revenue from two different sources and visualizes them together on a shared timeline.

## Overview

This notebook combines two data collection methods to compare Tesla's share price against its reported revenue over time: stock price pulled via the `yfinance` API and revenue figures scraped from an HTML page with BeautifulSoup.

## Note on files

`analyzing_data.ipynb` and `analyzing_historical_stock_revenue_data.ipynb` are identical copies of the same notebook.

## Workflow

1. **Extract stock data**: uses `yfinance` to pull Tesla's (`TSLA`) full historical share price data.
2. **Extract revenue data**: downloads an HTML page with `requests`, parses it with BeautifulSoup, and uses `pandas.read_html()` to pull Tesla's quarterly revenue table. Cleans the `Revenue` column by stripping commas and dollar signs and dropping empty/null rows.
3. **Define a graphing function**: builds a two-panel Plotly figure with shared x-axes showing historical share price on top and historical revenue below, and saves the chart to `plotly_graph.html`.
4. **Plot the result**: renders the combined stock price vs. revenue chart for Tesla.

## Technologies

- Python
- yfinance
- pandas
- BeautifulSoup (bs4)
- Plotly

## Getting Started

```bash
pip install yfinance bs4 nbformat pandas plotly
jupyter notebook analyzing_data.ipynb
```

## Author

Nurana Verdiyeva
