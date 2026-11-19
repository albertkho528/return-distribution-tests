# Is a Daily Return a Coin Flip?

Testing distribution assumptions on Bitcoin and China A-shares. Course project, Central University of Finance and Economics (Math, Fall 2026).

The coin-flip model treats each day's return as an independent trial with fixed odds and thin tails. This project tests five of its assumptions, using only the methods of Lecture Note 2 (Random Variables, Distributions, and Moments).

| Module | Assumption tested | Lecture method | Data |
|---|---|---|---|
| 1 | Up and down days are equally likely | Binomial, exact test, power | Bitcoin |
| 2 | Past days have no memory | Geometric, memoryless property | Bitcoin |
| 3 | Extreme days arrive at a constant rate | Poisson, mean = variance, exact test | Bitcoin |
| 4 | Returns have thin (normal) tails | Normal vs Laplace vs Cauchy, CDFs | Bitcoin |
| 5 | Returns can take any value | Mixed CDF with atoms at the price limits | RESSET A-shares |

## Data (not included in this repository)

- `data_raw/btc.csv`: Coin Metrics community data, https://github.com/coinmetrics/data/blob/master/csv/btc.csv (column `PriceUSD`). Sample: 2018-01-01 to 2025-12-31.
- `data_raw/resset/`: RESSET Financial Research Database (锐思金融研究数据库), Daily Merged Stock Data (DRESSTK), Shanghai and Shenzhen main-board A-shares, 2024-01-01 to 2025-12-31. RESSET is licensed through an institutional subscription and its terms forbid redistributing the data, so the files are not included here.

## Structure

| Folder | Contents |
|---|---|
| `data_raw/` | Downloaded files, never edited |
| `data_clean/` | Files saved by the notebooks |
| `notebooks/` | One notebook per step, run in order |
| `outputs/` | Figures and tables used in the presentation |

## Roadmap

- **v1 (Dec 2026):** the five modules above, Lecture Note 2 methods only.
- **v2:** the same assumptions tested with methods from later in the course.
