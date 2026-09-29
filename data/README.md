# Data files

All paths in the chapters are relative to the repository root (e.g. `read.xlsx("data/dfx_2.xlsx")`),
so knit the `.Rmd` files with the working directory set to the repo root.

## Files used by the book

The published book (https://www.arturo-bernal.com/book/AFP/index.html) downloads the
`.csv` files straight from this repo, for example
`read.csv("https://raw.githubusercontent.com/abernal30/BookAFP/main/data/df_dates.csv")`.
**Do not rename, move or delete these files**, or the published book's code will break.

| Chapter | `.Rmd` in this repo reads | Published book reads (raw GitHub URL) |
|---|---|---|
| 01 R Basics | `data_df.xlsx`, `df5.xlsx`, `df5.csv` (written and re-read to compare formats) | — |
| 02 Data cleaning | `credit_semioriginal.xlsx` | `credit_semioriginal.csv`, `credit_semioriginal_num.csv` |
| 06 Credit analysis | `credit_short.xlsx` | `credit.csv` |
| 07 Rational agent theory | `df_dates.xlsx` | `df_dates.csv` |
| 08 Momentum strategy | `dfx_2.xlsx` | `price_momentum_orig.csv`, `ret_momentum_orig.csv` |
| 09 Portfolio management | `df_merge.xlsx`, `dfx_2.xlsx` | `df_merge.csv`, `dfx_2.csv` |

Chapters 03, 04 and 05 download their data from APIs / the web (quantmod, Quandl, rvest).

The `.csv`/`.xlsx` pairs (`credit_semioriginal`, `df_dates`, `dfx_2`, `df_merge`) hold the same
data. If you edit one, update the other.

## Other datasets

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
