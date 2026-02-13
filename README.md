# Trader_sentiment_analysis
🎯 Objective

Analyze how Bitcoin market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid, and derive actionable strategy insights.

📂 Datasets

Bitcoin Market Sentiment (Fear/Greed Index)
Historical Trader Data (Hyperliquid transactions)
Data was aligned at the daily level.

⚙️ Methodology

Cleaned and standardized column names.
Converted timestamps and aligned both datasets on daily date.

Engineered key metrics:
Daily PnL per trader
Win rate
Trade frequency
Position size
Behavioral segments (frequent/infrequent, consistent/inconsistent)
Compared performance under Fear vs Greed regimes.
Built a Random Forest classifier to predict trade profitability using sentiment + behavioral features.

📈 Key Insights

Performance differs across sentiment regimes
PnL distribution and volatility vary between Fear and Greed days, indicating sentiment-driven risk exposure.

Traders modify behavior during Greed periods
Trade frequency and position sizes tend to increase during Greed regimes.

Behavioral segmentation reveals risk concentration
High-activity and high-volatility traders exhibit larger drawdowns during Fear periods.

Predictive modeling shows moderate signal (60% accuracy)
The model predicts losing trades more reliably than profitable ones, suggesting sentiment features are more useful for risk filtering than alpha generation.

💡 Strategy Recommendations

Strategy 1 – Dynamic Risk Adjustment
Reduce leverage and position size during Fear periods, particularly for high-activity traders.

Strategy 2 – Trade Filtering Rule
Use predictive model probabilities to filter out high-risk trades instead of aggressively selecting profitable ones.

▶ How to Run
pip install -r requirements.txt

Open the notebook:
jupyter notebook notebooks/trader_sentiment_analysis.ipynb
