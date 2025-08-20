 # nifty50-time-of-day-analysis
This project analyzes NIFTY50 intraday volatility using 5-minute data. By combining volatility heatmaps with technical indicators, it identifies high-opportunity time slots. A rule-based backtest shows that aligning strategies with these periods improves performance, reduces risk, and bridges analysis with real trading.

# PROJECT - 
 
# ⏰ Time-of-Day Analysis of NIFTY50 Index

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data--Analysis-lightgrey?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?logo=plotly)

---

## 📊 Project Overview
This project analyzes **intraday volatility of the NIFTY50 index** using high-frequency (5-minute and 15-minute) data to uncover recurring patterns in market behavior.  
By combining **volatility heatmaps** with widely used **technical indicators** (RSI, MACD, VWAP, ADX, SuperTrend), the study highlights high-probability trading time slots and evaluates systematic rule-based strategies.  

The goal is to build a **data-driven, time-aware intraday trading framework** that improves win percentage, profitability, and risk-adjusted performance compared to random or uniformly timed trades.

---

## ⚙️ Methodology
1. **Data Collection**  
   - 5-minute OHLCV data (2015–2025) from NSE.  
   - Filtered valid trading hours (09:15–15:30), weekdays only.  

2. **Volatility Heatmaps**  
   - Metrics: High–Low fluctuation & absolute price movement.  
   - Grouped by **weekday × time slot** to reveal patterns.  

3. **Technical Indicators**  
   - RSI, MACD, VWAP, ADX, SuperTrend.  
   - Trade signals filtered by high-volatility slots.  

4. **Trading Framework**  
   - Fixed SL/TP (e.g., 20-point SL, 40-point TP).  
   - Trailing SL for dynamic exits.  
   - Position sizing for risk management.  
   - Max **2 trades per day**.  

5. **Backtesting & Evaluation**  
   - Compared **slot-aware trades vs random trades**.  
   - Metrics: Win rate, Avg/Total PnL, Sharpe ratio, Drawdown.  
   - Parameter sweep for optimal SL/TP.  

---

## 📊 Key Findings
- **High Volatility Slots**:  
  - 09:15–10:00 AM & 03:00–03:30 PM showed strongest volatility.  
  - Mondays & Fridays more volatile due to weekend gaps & adjustments.  

- **Low Volatility Slots**:  
  - Midday (12:00–14:00) → range-bound, less profitable.  

- **Indicator Alignment**:  
  - RSI alone ≈ 49% accuracy.  
  - RSI + High-Vol Slots ≈ 54% accuracy.  

- **Strategy Performance**:  
  - Slot-aware strategies outperformed random ones.  
  - Trailing SL worked best in volatile sessions.  
  - Fixed SL/TP better in stable sessions.  

---

## ✅ Conclusion
- Intraday volatility is **not uniform** — time-of-day plays a key role in market behavior.  
- Slot-aware trading **reduces noise** and improves accuracy.  
- Aligning trades with volatility windows → **higher profitability & lower risk**.  
- The project bridges **data exploration & real-world algorithmic trading**.  

---

## 🚀 Future Enhancements
- Apply **Machine Learning models** (LSTM, XGBoost, Random Forest) for predictive volatility.  
- Extend analysis to **Bank NIFTY, Sensex, and stocks**.  
- Build a **real-time alert system** with live NSE feeds.  
- Integrate **news sentiment analysis** with time-slot analysis.  
- Develop an **interactive dashboard** (Streamlit/Dash).  
- Use **advanced optimization** (Bayesian, GA) for SL/TP tuning.  

---

## 📚 References
1. Murphy, J.J., *Technical Analysis of the Financial Markets*. NYIF, 1999.  
2. Chan, E.P., *Algorithmic Trading: Winning Strategies and Their Rationale*. Wiley, 2013.  
3. [NSE India](https://www.nseindia.com)   
4. [GoCharting](https://gocharting.com)  

---
## 📁 Repository Structure
- `nifty50_5min.csv` – Raw 5-minute candlestick data.  
- `resampled_15min_data.csv` – 15-minute resampled data.  
- `SMA3.ipynb` – Main notebook with full analysis and visualizations.  
- `heatmap_avg_diff.csv`, `heatmap_abs_move.csv` – Data for volatility heatmaps.  
- `high_volatility_slots.csv` – Identified high-volatility slots.  
- `output899.jpg` – Heatmap visualization output.  

- **Trading Strategy Logs:**
  - `adjusted_trades.csv`, `final_adjusted_trades.csv`  
  - `backtest_trades.csv`, `daily_stats.csv`  
  - `phase3_trades_with_tp_sl.csv`, `phase4_trades_trailing_stop.csv`  
  - `phase5_trades_position_sizing.csv`, `phase5_trades_position_sizing_best_combo.csv`  
  - `slot_trades.csv`, `parameter_sweep_results.csv`  
- `requirements.txt` – List of Python dependencies for running the notebook.  
- `sai_report.pdf` – Full report documenting the project.  



