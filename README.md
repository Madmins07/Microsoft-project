<div align="center">
  <img src="assets/banner.svg" alt="Market Scraper. Yahoo Finance scraper: quotes, gainers, losers, a CSV portfolio, and headlines." width="100%"/>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/python-3.10+-A6BDAD?style=flat-square&labelColor=0B0E0D&logo=python&logoColor=EEF1ED" alt="python 3.10+"/>
  <img src="https://img.shields.io/github/last-commit/Madmins07/Microsoft-project?style=flat-square&labelColor=0B0E0D&color=788A7F&label=updated" alt="last-commit"/>
  <img src="https://img.shields.io/github/license/Madmins07/Microsoft-project?style=flat-square&labelColor=0B0E0D&color=5A6A60" alt="license"/>
</div>

## about

A Yahoo Finance scraper in plain Python: `requests` fetches the page, `BeautifulSoup` pulls the numbers, `tabulate`
prints them, and CSV files keep state between runs.

| function | what |
|:--|:--|
| `fetchStock('AAPL,MSFT')` | Name, intraday price, change and change percent for each symbol. |
| `fetchtop()` / `fetchloss()` | Live top gainers and losers; also refreshes `gainers.csv` / `losers.csv`. |
| `addtoPortfolio()` / `refreshPortfolio()` | Build a holdings list in `portfolio.csv` and re-price it live. |
| `Newsletter()` | Headlines from the Yahoo Finance front page. |

## run

```bash
pip install -r requirements.txt
python -c "import data_fetch_store as m; print(m.fetchStock('AAPL,MSFT'))"
```

## caveat

Scrapers track someone else's markup. Yahoo changes theirs often, so expect to adjust the selectors. The three CSVs
are sample outputs from when it was written.

---

<div align="center">
  <sub>Part of <a href="https://github.com/Madmins07">Madmins07</a> · Madhav Agarwal · IIT Kharagpur</sub>
</div>
