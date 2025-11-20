# Analysis of Trading Behaviour in Relation to Market Sentiment (Fear vs Greed)

Data Science Internship Assignment – Web3 Trading Team

Candidate: Anshika Dubey

# Abstract

Financial markets are not driven only by numbers; they are heavily shaped by human emotions. This project explores how trader behaviour on the Hyperliquid trading platform changes in response to market sentiment measured using the Bitcoin Fear & Greed Index. By analyzing profitability, trading activity, volume, and directional bias under different sentiment conditions, this study reveals important behavioural patterns and hidden trends that can be used to design more informed and discipline-driven trading strategies.

# 1. Problem Objective

The main objective of this project is to:

Analyze how trading behaviour — in terms of profitability, risk-taking, volume, and directional bias — aligns with or diverges from overall market sentiment classified as Fear or Greed. Furthermore, the study aims to uncover hidden trends and signals that could contribute to smarter, more adaptive trading strategies in Web3 markets.

# 2. Datasets Overview

Two datasets were used for this analysis:

2.1 Bitcoin Market Sentiment Dataset

This dataset contains daily classifications of market sentiment, categorized as:

- Fear

- Neutral

- Greed

- Extreme Fear

- Extreme Greed

The columns used were:

- Date

- Classification

This dataset reflects the collective psychological state of market participants.

2.2 Hyperliquid Historical Trading Dataset

This dataset contains trade-level information. The key columns used in the analysis include:

closed_pnl – Profit or loss per trade

size_usd – Trading volume in USD

size_tokens – Token quantity traded

side / side_num – Long or Short position

start_position – Initial exposure

account – Used to count number of trades

date, time, hour, minute – Timestamp information

The raw data was transformed into daily aggregated metrics for meaningful comparison with daily sentiment.

# 3. Data Processing and Methodology

The analysis was conducted in the following stages:

3.1 Data Preprocessing

All column names were standardized.

Timestamp columns were converted into proper datetime format.

Rows with missing or invalid dates were removed.

3.2 Feature Engineering

For each day, the following metrics were calculated:

- Total daily profit and loss (PnL)

- Average profit per trade

- Total trading volume (USD and Tokens)

- Number of trades executed

- Net trade direction (Long vs Short bias)

- Average position size (as a proxy for risk)

3.3 Data Integration

The aggregated daily trading data was then merged with the Bitcoin Fear & Greed Index on the basis of date to align trading behaviour with corresponding market sentiment.

3.4 Analysis Techniques

The analysis included:

- Correlation testing

- Distribution analysis

- Time series visualization

- Sentiment-based comparisons

- Top-performance day evaluation

# 4. Key Findings Based on Trading Behaviour
4.1 Profitability vs Market Sentiment

One of the most interesting results was related to daily profitability:

Although Greed is typically associated with opportunity, many of the most profitable days actually occurred during Fear conditions.

Extreme Greed periods showed very large profits in some cases, but also some of the largest losses.

Neutral days were generally associated with smaller profit and loss ranges.

Insight:
Market Fear, while typically seen as negative, can offer powerful trading opportunities due to increased volatility and strong price reversals.

4.2 Risk Behaviour and Directional Bias

Risk was analysed using start_position and net_direction.

During Greed and Extreme Greed, the net direction was strongly positive, meaning that traders were heavily biased toward LONG positions.

During Fear, the direction was more unstable and mixed, showing hesitation and uncertainty.

Extreme sentiment conditions (both Fear and Greed) produced the most extreme directional values.

Insight:
Traders tend to become more emotional and aggressive during strong sentiment periods, which increases exposure and risk.

4.3 Volume and Trading Frequency

The number of trades and total volume showed clear behavioural patterns:

High trading volumes were observed during both Fear and Greed

Neutral periods showed significantly lower volume and participation

Large spikes in activity were seen during major sentiment shifts

Insight:
Traders are more reactive to emotional market conditions than to calm or neutral markets.

4.4 Correlation Analysis

Correlation results showed:

Strong positive correlation (≈0.7) between number of trades and total profit

Weak negative correlation between profit and trade direction

Almost no correlation between net direction and trade frequency

Insight:

Profitability is much more closely related to trading activity and consistency than to simply being long or short.

This means participation and timing are more important than direction alone.

# 5. Hidden Patterns Discovered

The visualization and analysis revealed several important hidden trends:

Fear often creates high-reward opportunities
Some of the best profit days occurred when the market sentiment was fearful.

Extreme Greed leads to dangerous overconfidence
Traders tend to over-leverage and take excessive risk, leading to major losses.

Volume is emotion-driven
Market sentiment strongly influences how actively traders participate.

Direction does not guarantee success
Strong long bias does not ensure high profit.

Sentiment shifts act as triggers
Rapid changes in sentiment coincide with spikes in trading activity.

These insights are essential for designing smarter strategies.

# 6. Strategic Implications

Based on this analysis, the following sentiment-based strategy can be suggested:

Market Sentiment	Suggested Trading Approach
Extreme Greed	Reduce risk, secure profits, avoid over-leverage
Greed	Trend following with careful risk management
Neutral	Low activity, wait for clear signals
Fear	Look for value entries with strong risk control
Extreme Fear	Trade cautiously, prepare for volatility/reversals

This emotion-aware strategy helps avoid impulsive decisions and aligns actions with data-backed patterns.

# 7. Limitations

The dataset does not include direct BTC price movement features.

Trader-level psychology cannot be directly observed.

Leverage data was not fully available.

The analysis is historical and not predictive by itself.

Future improvements could include volatility indicators, technical analysis, and machine learning prediction models.

# 8. Conclusion

This project demonstrates that trading behaviour is strongly influenced by market sentiment. Emotional states such as Fear and Greed directly impact how traders take risk, how much volume they trade, and how profitable they become. Contrary to popular belief, some of the largest opportunities arise in fearful markets, whereas the most dangerous losses tend to occur in extreme greedy conditions.

By identifying these hidden behavioural patterns, this study provides valuable insights that can be used to build more intelligent, disciplined, and data-driven trading strategies in cryptocurrency and Web3 markets.
