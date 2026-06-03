# 📈 NSE Option Chain Analyzer

> Real-time NSE option chain fetcher and visualizer for NIFTY & HDFCBANK — auto-refreshes every 3 minutes and plots Open Interest (OI) and Implied Volatility (IV) for the top strike prices.

---

## 🧠 What This Does

Options traders need to track OI and IV across strike prices to gauge market sentiment and spot large positions. This notebook automates that — it pulls live data directly from NSE, filters the most relevant strikes around the current price, stores snapshots locally, and visualizes them in clean charts.

---

## ✨ Features

- 📡 **Live NSE Data** — Fetches real-time option chain data for NIFTY and HDFCBANK
- 🎯 **Smart Strike Filtering** — Automatically selects 5 strikes above and below the current price
- 💾 **Local JSON Storage** — Saves each snapshot for historical comparison
- 📊 **OI & IV Charts** — Visualizes Open Interest and Implied Volatility side by side
- 🔁 **Auto-Loop** — Refreshes every 3 minutes during market hours

---

## 🛠 Tech Stack

- **Python 3**
- **Jupyter Notebook**
- `requests` — API calls to NSE
- `pandas` — Data parsing and filtering
- `matplotlib` / `seaborn` — Visualization
- `json` — Local data storage

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
# Clone the repo
git clone https://github.com/prakritipatkar/NSE_Option_Chain_Data.git
cd NSE_Option_Chain_Data

# Install dependencies
pip install requests pandas matplotlib seaborn jupyter

# Launch notebook
jupyter notebook main.ipynb
```

---

## 📁 Project Structure

```
NSE_Option_Chain_Data/
├── main.ipynb                  # Main notebook — run this
├── NIFTY_option_chain.json     # Saved NIFTY snapshot
└── HDFCBANK_option_chain.json  # Saved HDFCBANK snapshot
```

---

## 📊 Sample Output

The notebook produces charts like:

- **OI Chart** — Calls vs Puts open interest across strikes (shows where big positions are)
- **IV Chart** — Implied volatility smile/skew across strikes

> _Add chart screenshots here_

---

## ⚠️ Notes

- NSE blocks direct API calls from servers — run locally during market hours (9:15 AM – 3:30 PM IST)
- Data is fetched using session headers mimicking a browser request
- For production use, consider adding proxy rotation

---

## 🔮 Future Improvements

- [ ] Max Pain calculation
- [ ] PCR (Put-Call Ratio) tracker
- [ ] Streamlit dashboard for non-technical users
- [ ] Historical OI trend charts

---

## 👩‍💻 Author

**Prakriti Patkar** — [LinkedIn](https://www.linkedin.com/in/prakriti-patkar-33125b228) · [GitHub](https://github.com/prakritipatkar)
