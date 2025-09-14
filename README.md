# Stock Market Trend Analysis & Predictive Insights

Analyze historical trends and predict future price movements of top Indian stock market companies using Python, statistical analysis, machine learning, and rich visualizations.

***

## 📚 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Setup & Requirements](#setup--requirements)
- [Workflow Description](#workflow-description)
- [Technical Features & Indicators](#technical-features--indicators)
- [Visualization & Analysis](#visualization--analysis)
- [Sentiment Analysis](#sentiment-analysis)
- [Price Prediction Modeling](#price-prediction-modeling)
- [Batch Modeling & Performance Table](#batch-modeling--performance-table)
- [Interactive Dashboards](#interactive-dashboards)
- [FAQ](#faq)
- [References](#references)
- [License](#license)

***

## 📝 Overview

This project provides an end-to-end pipeline on historical stock data for **10 leading NSE companies** (Reliance, TCS, Infosys, HDFC Bank, ICICI Bank, Bharti Airtel, Hindustan Unilever, SBI, Kotak Mahindra Bank, ITC).

You get:  
- Automated data fetching, pre-processing, and feature engineering  
- Multiple technical indicators  
- Machine learning-based price prediction  
- Interactive visualization in Matplotlib & Plotly  
- Sentiment analysis with TextBlob  
- Easily extendable code for additional analytics and Indian (NSE) securities  

***

## 🚀 Key Features

- **Historical Data Download**: 5 years for 10 major NSE stocks using `yfinance`
- **Automated Feature Engineering**: Calculating SMA, EMA, RSI, Bollinger Bands, etc.
- **Visualization**: Classic plots (Matplotlib) + Interactive (Plotly)
- **Model Training & Evaluation**: Linear regression for price prediction (per stock and all at once)
- **Sentiment Analysis**: Scores company news headlines
- **Batch Results Table**: RMSE and regression coefficients for all stocks

***

## ⚙️ Setup & Requirements

**Install Python libraries** (Colab or local):

```python
!pip install yfinance matplotlib pandas scikit-learn textblob vaderSentiment seaborn plotly
```

**Extra**:  
- Jupyter Notebook or Google Colab recommended

***

## 🛠️ Workflow Description

1. **Setup & Library Installation**
   - Ensures all required libraries are present.

2. **Select Stocks**
   - Processes a fixed list of blue-chip NSE tickers.

3. **Download, Save & Preprocess**
   - Historical prices (`yfinance`), stored as CSV per stock.
   - Feature engineering: rolling mean (SMA), returns, etc.

4. **Generate Additional Indicators**
   - EMA, RSI-14, Bollinger Bands, returns for technical analysis.

***

## 📈 Technical Features & Indicators

Calculated for each stock:
- SMA (50-day)
- EMA (20-day)
- RSI (14-day)
- Bollinger Upper/Lower bands (20, 2 std)
- Daily returns

Indicators appended to each stock's processed CSV.

***

## 🖼️ Visualization & Analysis

- **Matplotlib**:  
  - Trends: Close price, SMA, other technicals for selected stocks.
- **Plotly**:  
  - Interactive candlestick charts with SMA/EMA layering
  - Interactive RSI bands with highlighted overbought/oversold zones

***

## ✒️ Sentiment Analysis

Applies TextBlob polarity on example news headlines for each company:

Sample Output:
```
Headline: Reliance Industries posts record quarterly results.
Sentiment Score: 0.00
Headline: ITC shares jump as market sentiment improves.
Sentiment Score: 0.00
Headline: HDFC Bank suffers losses after regulatory action.
Sentiment Score: -0.25
```

***

## 🤖 Price Prediction Modeling

- **Single stock example**:  
  Linear regression using SMA as feature, predicting Close Price.
  - Automatic split: 80% train, 20% test
  - RMSE reported

- **Batch (all stocks)**:  
  Loops through each ticker, fits regression, outputs RMSE and coefficient.

**Sample result table:**

| Ticker        | Test_RMSE | Coefficient |
|--------------|-----------|-------------|
| RELIANCE.NS  | 78.36     | 1.00        |
| TCS.NS       | 238.77    | 0.99        |
| INFY.NS      | 104.92    | 0.93        |
| ...          |    ...    | ...         |

***

## 📊 Interactive Dashboards

- **Plotly Candlestick Chart**: with SMA, EMA overlays (last ~10 months)
- **RSI Interactive Line**: with "overbought" (70) and "oversold" (30) lines

***

## ❓ FAQ

**Q: Can I try different stocks?**  
A: Yes, just add their tickers in the stock list section.

**Q: Where are the predictions saved?**  
A: All calculated features and predictions are stored as CSV output files per ticker.

**Q: What if a ticker has no data?**  
A: The script skips missing tickers and continues with the available ones.

**Q: Can I use this in Power BI?**  
A: Yes. Exported CSVs can be imported into Power BI for further dashboarding.

***

## 🔗 References

- [`yfinance` documentation](https://github.com/ranaroussi/yfinance)
- [`scikit-learn` regression docs](https://scikit-learn.org/stable/modules/linear_model.html)
- [NSE](https://www.nseindia.com/)

***

## 📄 License

MIT License

***

## 📬 Contact

For improvements, issues, or collaboration:  
vinaykumar031vk@gmail.com

***

[1](https://github.com/imvinxx/Stock_Market_Trend_Analysis_and_Predictive_Insights/raw/refs/heads/main/Stock_Market_Trend_Analysis_&amp;_Predictive_Insights.ipynb)
[2](https://github.com/imvinxx/Stock_Market_Trend_Analysis_and_Predictive_Insights/edit/main/Stock_Market_Trend_Analysis_%26_Predictive_Insights.ipynb)
