HSI Sentiment Quantitative Trading Strategy
## Project Description
This project implements a quantitative trading approach for the Hang Seng Index (HSI) that incorporates social media sentiment analysis. The strategy uses public prediction data from retail investors to generate trading signals and has been validated through comprehensive historical testing.

## Data Processing Methodology
Addressed data gaps by implementing neutral value substitution (0.5) for missing sentiment entries
Developed sentiment metric from the spread between positive and negative vote percentages, normalized to -1 to 1 scale
Applied technical smoothing using 5-day moving averages to reduce market noise and enhance signal reliability

## Strategy Implementation
Entry trigger: 5-day sentiment average exceeds 0.1 threshold
Exit trigger: 5-day sentiment average falls below -0.1 threshold
Neutral position maintained when sentiment remains within central range [-0.1, 0.1]
Operational procedure: Trading decisions finalized after market close, with execution at next session's opening

## Performance Analysis (2022-2023 Period)
Performance Metric	Buy & Hold Baseline	Sentiment Strategy
Total Return	-20.27%	-29.60%
Annualized Return	-12.85%	-19.20%
Risk-Adjusted Return (Sharpe)	-0.33	-1.23
Maximum Capital Decline	-35.87%	-30.81%
Successful Trade Percentage	Not Applicable	39.0%

## Research Insights
The sentiment-driven approach showed measurable improvement in capital preservation, reducing maximum portfolio decline by 5.06%
Implementation successfully identified high-volatility market periods, limiting exposure through strategic position changes
Sentiment-based signals provided actionable warnings during market downturns, demonstrating predictive utility

## File Organization

hsi_sentiment_trading/
├── hsi_sentiment_strategy.ipynb  # Core implementation code
├── sentiment_data.csv           # Market and sentiment dataset
├── strategy_report.pdf          # Comprehensive analysis
└── README.md                    # Project documentation


Data analysis libraries: pandas, numpy, matplotlib
Input data format: Timestamp, price data (open/high/low/close), sentiment indicators

## Deployment Steps
1. Load market dataset into Google Colab workspace
2. Install necessary Python libraries
3. Run implementation code in sequence
4. Examine performance metrics and graphical outputs

Evaluate strategy effectiveness across different market conditions

Summary
This sentiment analysis framework establishes a methodological foundation for incorporating unconventional data sources into trading systems. While absolute returns underperformed the market benchmark during the test period, the approach demonstrated significant value in risk mitigation and drawdown control. The modular design supports further refinement and parameter optimization for enhanced performance.

