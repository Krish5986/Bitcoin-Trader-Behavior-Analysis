# 📊 Bitcoin Trader Behavior Analysis

## 🚀 Project Overview
This project analyzes how Market Sentiment (Fear & Greed Index) impacts trader behavior and profitability on the Hyperliquid exchange.  
By merging 211k+ trade records with daily sentiment data, we uncover behavioral patterns, risk dynamics, and actionable trading rules.

The analysis focuses on:
- Performance differences across sentiment regimes
- Behavioral shifts in risk-taking and long/short bias
- Segmentation of traders into behavioral archetypes
- Actionable strategy design

**Technologies:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn (K-Means)

---

## 📂 Repository Contents
- `Primetrade_Trader_Analysis.ipynb` → Main analysis notebook  
- `README.md` → Project overview and insights  

---

## ▶️ How to Run
1. Open `Primetrade_Trader_Analysis.ipynb` in Google Colab or Jupyter Notebook  
2. Update dataset paths if needed  
3. Run all cells top-to-bottom  

---

## 💡 Key Insights

### 1. The “Fear” Paradox
- Traders are predominantly **buying (~51%) during Extreme Fear** and **selling during Extreme Greed** (contrarian behavior).
- The **highest average Closed PnL per trade (~$67.9)** occurs during **Extreme Greed**, followed by **Fear**.
- Neutral markets are the least profitable.

### 2. Winner vs Loser Psychology
- **Losers:** Bet their largest position sizes (~$8,190) during panic, often catching falling knives.  
- **Winners:** Reduce size during downturns (~$4,414) and scale up aggressively (~$9,612) only during Greed.

### 3. Risk Exposure
- The dataset does not contain an explicit leverage field.  
- **Position size (USD) is used as a proxy for risk exposure.**  
- Risk-taking increases during Greed and Extreme Greed.

---

## 📉 Drawdown Proxy
Worst daily PnL per trader is used as a drawdown proxy, showing heavy negative tails for many traders, highlighting the importance of risk controls.

---

## 🤖 Bonus: Trader Archetypes (Clustering)

Using K-Means clustering on average PnL, win rate, position size, and trade count:

- 🐳 **Whales** – Very large sizes, moderate frequency  
- 🎯 **Snipers** – Higher win rate, low frequency  
- 🤖 **Bots** – Extremely high frequency, low PnL per trade  
- 👥 **Crowd** – Low volume, small sizing, average performance  

---

## 📈 Actionable Strategies

| Strategy | Trigger | Action | Logic |
|--------|--------|--------|------|
| Anti-Panic Protocol | Index < 25 (Extreme Fear) | Hard cap position size to 50% | Prevents revenge trading and large losses |
| Trend-Surfer Protocol | Index > 60 (Greed) | Increase size limits + use trailing stop | Exploit most profitable regime |

---

## ⚠️ Notes
- A Welch t-test between Fear and Greed PnL shows a **directional difference but not statistically significant at 5% (p ≈ 0.064)**.  
- Results should be interpreted as strong empirical patterns rather than guaranteed edges.

---

## 📬 Contact
For questions or collaboration, feel free to reach out.
