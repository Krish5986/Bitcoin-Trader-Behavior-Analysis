# 📊 Bitcoin Trader Behavior Analysis

## 🚀 Project Overview
This project analyzes how **Market Sentiment (Fear & Greed Index)** impacts trader behavior and profitability on the Hyperliquid exchange. 
By merging 200k+ trade records with daily sentiment data, we identified profitable "Contrarian" strategies and segmented traders into behavioral archetypes using K-Means Clustering.

**Technologies:** Python, Pandas, Seaborn, Scikit-Learn (K-Means).

---

## 💡 Key Insights

### 1. The "Fear" Paradox
* **Insight:** Traders are **predominantly Buying (51%)** during "Extreme Fear" (Index < 25) and **Selling** during "Extreme Greed".
* **Profitability:** Paradoxically, the highest average profit per trade (**$67.89**) occurs during "Extreme Greed", followed closely by "Fear". "Neutral" markets are the least profitable.

### 2. Winner vs. Loser Psychology
* **Losers:** Tend to bet their largest position sizes (**$8,190**) during Panic events, often "catching falling knives."
* **Winners:** Manage risk better in downturns ($4,414 avg size) and bet big ($9,612) only when the trend is confirmed (Greed).

---

## 🤖 Bonus: Trader Archetypes (Clustering)
Using Unsupervised Learning (K-Means), we identified 4 distinct trader profiles:
* **🐳 The Whales:** Massive position sizes ($5,900+), selective trading.
* **🎯 The Snipers:** High Win Rate, low frequency.
* **🤖 The Bots:** Extreme trade frequency (18,000+ trades), low PnL per trade.
* **👥 The Crowd:** Low volume, small sizing, average performance.

---

## 📈 Actionable Strategies

| Strategy | Trigger | Action | Logic |
| :--- | :--- | :--- | :--- |
| **Anti-Panic Protocol** | Index < 25 (Extreme Fear) | **Hard Cap Position Size (50%)** | Prevents "Revenge Trading" during volatility, mimicking Winner behavior. |
| **Trend-Surfer Protocol** | Index > 60 (Greed) | **Increase Limits + Trailing Stop** | Maximizes upside during the most profitable market regime ($67/trade). |
