# MScFE 600 Financial Data - Group Work Project #1

## Overview
This Jupyter notebook contains a comprehensive analysis and discussion of financial data forecasting using machine learning techniques. The project focuses on predicting stock price movements using technical indicators for exchange-traded funds (ETFs).

## Project Contents

### 1. **Data Understanding (Q1)**
Explores the types of data and technical indicators used in the analysis:
- **Data Sources**: Daily market data from three ETFs:
  - ECH (Emerging Markets - Chile)
  - EWZ (Emerging Markets - Brazil)
  - IVV (Developed Markets - S&P 500)
- **Features**: 210+ technical indicators derived from OHLCV data using Pandas-TA library
- **Technical Indicator Categories**:
  - Momentum indicators (RSI, Stochastic)
  - Trend indicators (Correlation Trend, TTM)
  - Volatility indicators (Bollinger Bands)
  - Volume indicators (On-Balance Volume)
  - Cycles and statistical measures

### 2. **Security Understanding (Q2)**
Detailed analysis of the iShares Core S&P 500 ETF (IVV):
- **Fund Profile**: 
  - Launched: May 15, 2000
  - Assets Under Management: $760+ billion
  - Expense Ratio: 0.03%
  - Beta: ~1.0
- **Historical Performance**: Long-term appreciation from ~$50 (2009) to ~$698 (Jan 2026)
- **Classification Approach**: 
  - Binary prediction (up/down) instead of regression
  - Reduces overfitting and focuses on directional signals
  - Better suited for trading strategy decisions

### 3. **Methodology Understanding (Q3)**
Discusses the research methodology including:
- Data organization and preparation
- Feature selection techniques
- Model architecture and training approaches
- Alternative classification variable definitions

## Key Findings
- **Feature Selection**: Using only ~5% (≈11) of the original 216 features achieves similar or better accuracy
- **Accuracy Range**: 78-80% classification accuracy across ETFs
- **Computational Efficiency**: Reduced feature set improves model training speed and generalization

## Technical Implementation
The notebook includes:
- Data loading and preprocessing
- Technical indicator computation
- Feature engineering and selection
- Neural network model implementation
- Performance evaluation and visualization
- Statistical analysis and results interpretation

## Data Processing Pipeline
1. **Data Source**: Yahoo Finance historical data
2. **Feature Engineering**: 216 technical indicators computed via Pandas-TA
3. **Data Normalization**: Min-Max scaling to [0, 1]
4. **Data Cleaning**: Missing values removed
5. **Target Variable**: Binary classification (next-day price up/down)

## Tools and Libraries
- Pandas and Pandas-TA for technical indicator computation
- NumPy for numerical operations
- Scikit-learn for feature selection and preprocessing
- TensorFlow/Keras for neural network modeling
- Matplotlib/Plotly for visualization

## How to Use
1. Ensure all required libraries are installed
2. Run cells sequentially from top to bottom
3. The notebook is organized in logical sections for easier understanding
4. Outputs include visualizations and statistical summaries

## Learning Objectives
By reviewing this notebook, you will understand:
- How technical indicators are derived from price data
- The importance of feature selection in financial machine learning
- Why classification is often preferred over regression for directional forecasting
- Best practices for financial time series analysis
- Model evaluation techniques for trading applications

## Notes
- All cells are markdown or Python code cells
- The analysis focuses on short-term (daily) price movements
- Results emphasize generalization and out-of-sample performance
- The approach is applicable to various financial instruments beyond the ETFs analyzed

---
**Course**: MScFE 600 - Financial Data  
**Project**: Group Work Project #1  
**Focus**: Machine Learning for Financial Forecasting
