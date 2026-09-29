# Data files

All paths in the chapters are relative to the repository root (e.g. `read.xlsx("data/dfx_2.xlsx")`),
so knit the `.Rmd` files with the working directory set to the repo root.

## Files read by the book chapters

| Chapter | File read | Same data also provided as |
|---|---|---|
| 01 R Basics | `data_df.xlsx`, `df5.xlsx`, `df5.csv` (written and re-read to compare formats) | — |
| 02 Data cleaning | `credit_semioriginal.xlsx` | `credit_semioriginal.csv` |
| 06 Credit analysis | `credit_short.xlsx` | — |
| 07 Rational agent theory | `df_dates.xlsx` | `df_dates.csv` |
| 08 Momentum strategy | `dfx_2.xlsx` | `dfx_2.csv` |
| 09 Portfolio management | `df_merge.xlsx`, `dfx_2.xlsx` | `df_merge.csv`, `dfx_2.csv` |

Chapters 03, 04 and 05 download their data from APIs / the web (quantmod, Quandl, rvest).

The `.csv` twins hold the same data as the `.xlsx` files the chapters read. They are kept for
readers who work in Python, Excel or other tools. If you edit one, update the other.

## Supplementary datasets (not read by any chapter)

| File | Contents |
|---|---|
| `credit.csv` | LendingClub loans (873 rows), `Default` target + categorical variables already coded as numbers |
| `credit_semioriginal_num.csv` | `credit_semioriginal` with categorical variables coded as numbers (output of `dataclean::asnum`) |
| `price_momentum_orig.csv` | Daily closing prices of growth stocks (SHOP, SQ, SE, NIO, ...) from 2019-11-11 |
| `ret_momentum_orig.csv` | Daily returns of the same stocks |
| `spSTF.csv` | Daily prices of large-cap US stocks (AAPL, MSFT, GOOG, ...) from 2020-01-02 |
| `data_mod.csv` | Company bankruptcy data (6,819 firms), `Bankrupt` target + financial ratios |
| `us_bond_yield.csv` | US Treasury yield curve (1 Mo to 30 Yr), daily from 2018-01-02 |
| `bonds2.csv` | Mexican government bonds (CETES) — name, term, clean/dirty price, yield or coupon |
| `StockPricePrediction.ipynb` | Python notebook: supervised-learning models to predict weekly MSFT returns |

## dataclean package

Chapters 02 and 06 use `dataclean`, which is not on CRAN. Install it once with:

```r
remotes::install_github("abernal30/dataclean")
```
