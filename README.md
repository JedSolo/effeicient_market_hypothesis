**Replications**
Most of the data used are proxies that are similar to the actual data used.

**The Challenge**

Most of the datasets from those papers are:

Either time-series price/return data (which can often be pulled from Yahoo Finance, FRED, or EIA), or

Specialized datasets (like CDS spreads, entropy measures, niche cryptocurrencies) which may not be openly downloadable, but can often be proxied with public data.

Since I don't have access to external files, I will:

Identify the datasets each of your cited works used.

Download equivalent datasets (or closest proxies) in Python (using yfinance, pandas-datareader, etc.).

Use replication-ready code snippets for each dataset + method.

**Datasets From Key References and their Proxies**

Schindler (2010) - Securitized real estate (REIT indices, 1992-2009).
Data source: FTSE NAREIT, EPRA/NAREIT indices.
Proxy: U.S. REIT Index via Yahoo Finance (^RMZ).

Charif et al. (2017) - MENA equity markets.
Data source: Country indices (Saudi, UAE, Egypt, etc.).
Proxy: MSCI country indices (sometimes available via Yahoo as ETFs, e.g., EGPT for Egypt, QAT for Qatar).

Milosevic-Avdalovic (2017) - Balkan stock markets (January effect).
Data source: Belgrade Stock Exchange, regional indices.
Proxy: Harder to get directly; can use ETFs that track Eastern Europe (CEE, ERUS).

Onali & Goddard (2011) - European equity markets (fractal/Hurst).
Data source: FTSE, DAX, CAC 40, Euro Stoxx.
Proxy: Yahoo Finance tickers: ^FTSE, ^GDAXI, ^FCHI, ^STOXX50E.

Kilic (2023), Kim (2022) - Cryptocurrencies (Bitcoin, Ethereum, others).
Data source: CoinMarketCap, CryptoCompare.
Proxy: Yahoo Finance tickers: "BTC-USD", "ETH-USD".
Ariff (2017) - Spot vs options market integration (US equities).
Data source: OptionMetrics (subscription).
Proxy: Hard to replicate fully, but you can use CBOE VIX (^VIX) and S&P 500 (^GSPC) as partial indicators.
