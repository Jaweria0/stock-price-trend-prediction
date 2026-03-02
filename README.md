
<h1>Stock Price Trend Prediction Using Machine Learning</h1>
<br>

<div class="badges">
    <img src="https://img.shields.io/badge/Status-Completed-brightgreen" alt="Project Status">
    <img src="https://img.shields.io/badge/Python-3.11-blue" alt="Python">
    <img src="https://img.shields.io/badge/Pandas-1.5-orange" alt="Pandas">
    <img src="https://img.shields.io/badge/NumPy-1.27-blueviolet" alt="NumPy">
    <img src="https://img.shields.io/badge/Scikit--Learn-1.3-green" alt="Scikit-learn">
    <img src="https://img.shields.io/badge/XGBoost-1.7-red" alt="XGBoost">
    <img src="https://img.shields.io/badge/Matplotlib-3.8-orange" alt="Matplotlib">
    <img src="https://img.shields.io/badge/Seaborn-0.12-blue" alt="Seaborn">
</div>
<br>

<h2>Abstract</h2>
<p style="text-align:center;">
Stock market prediction is a challenging problem due to volatility, noise, and dynamic behavior. This project develops a machine learning classification system to predict short-term stock price direction using historical data and engineered technical indicators. Emphasis is placed on proper time-series validation and strict data leakage prevention. Logistic Regression, Random Forest, and XGBoost were trained and compared. Realistic accuracy after leakage removal stabilized around 48–51%, highlighting short-term forecasting difficulty.
</p>
<br>

<h2>Introduction</h2>
<p style="text-align:center;">
Financial markets are highly dynamic and influenced by multiple factors. Predicting stock price movement is valuable but challenging, particularly for short-term forecasting. This project builds a realistic machine learning pipeline to predict next-day stock price direction while following proper time-series modeling principles.
</p>
<br>

<h2>Objectives</h2>
<p style="text-align:center;">
<ul>
    <li>Collect, preprocess, and analyze historical stock data</li>
    <li>Engineer meaningful features for prediction</li>
    <li>Train and evaluate multiple machine learning models</li>
    <li>Visualize results and provide actionable insights</li>
    <li>Implement a leakage-free, robust evaluation framework</li>
</ul>
</p>
<br>

<h2>Dataset Description</h2>
<p style="text-align:center;">
Historical daily stock data covering 5–10 years collected from Yahoo Finance, Kaggle, and other sources. Core variables: <code>Date</code>, <code>Open</code>, <code>High</code>, <code>Low</code>, <code>Close</code>, <code>Volume</code>. Processed using Python libraries such as Pandas and NumPy.
</p>
<br>

<h2>Methodology</h2>

<h3>Data Preprocessing</h3>
<p style="text-align:center;">
Converted dates, sorted chronologically, removed missing and duplicate entries. Target variable defined as binary: 1 for upward, 0 for downward movement.
</p>
<br>

<h3>Feature Engineering</h3>
<p style="text-align:center;">
<pre>
- Daily returns, logarithmic returns, multi-day rolling returns
- Moving averages (SMA, EMA)
- Volatility measures
- Bollinger Bands
- Relative Strength Index (RSI)
- MACD
- On-Balance Volume
- Lag features shifted by one day
</pre>
</p>
<br>

<h3>Data Leakage Prevention</h3>
<p style="text-align:center;">
Removed target-derived columns and raw price values. Features were shifted to use only historical information. Applied chronological 80%-20% train-test split.
</p>
<br>

<h3>Model Training</h3>
<p style="text-align:center;">
Three models were trained and evaluated:
<pre>
- Logistic Regression: baseline linear model
- Random Forest: ensemble tree-based model
- XGBoost: gradient boosting with 400 estimators, learning rate 0.03, max depth 5
</pre>
</p>
<br>

<h2>Results and Evaluation</h2>
<p style="text-align:center;">
Accuracy after leakage removal: Logistic Regression ~51%, Random Forest ~48%, XGBoost ~49–50%. Feature importance: returns, RSI, MACD, volatility features most significant. Visualization and confusion matrix analysis further validated model performance.
</p>
<br>

<h2>Discussion</h2>
<p style="text-align:center;">
Short-term stock trend prediction is highly complex. Removing data leakage emphasized robust validation. Traditional ML models struggle with subtle nonlinear patterns in financial time-series data. Observed trends show that downward movements are slightly easier to predict than upward movements.
</p>
<br>

<h2>Limitations</h2>
<p style="text-align:center;">
Does not include macroeconomic indicators, sentiment analysis, deep learning sequence models, or trading strategy backtesting. Hyperparameter tuning was limited.
</p>
<br>

<h2>Future Work</h2>
<p style="text-align:center;">
Future improvements include:<br>
<ul>
    <li>Integrating news sentiment analysis and macroeconomic variables</li>
    <li>Implementing LSTM, GRU, or Transformer models for sequence prediction</li>
    <li>Applying walk-forward validation and robust cross-validation</li>
    <li>Developing simulated trading strategies to evaluate real-world profitability</li>
    <li>Enhancing feature engineering with advanced technical and market indicators</li>
</ul>
</p>
<br>

<h2>Conclusion</h2>
<p style="text-align:center;">
This project successfully developed a robust, leakage-free ML pipeline for short-term stock price trend prediction. Models achieved ~50% accuracy, reflecting the inherent difficulty of forecasting. The main achievement lies in implementing realistic validation and avoiding data leakage. The framework provides a strong foundation for future research and real-world trading simulations.
</p>
<br>

<h2>Contributors</h2>
<p style="text-align:center;">
The following team members collaboratively developed this project:
</p>
<div class="contributors">
    <div class="contributor"><strong>Usama:</strong> Data Collection & Management – collected and cleaned historical stock data.</div>
    <div class="contributor"><strong>Nimra:</strong> Data Preprocessing – handled missing values, normalization, and prepared processed datasets.</div>
    <div class="contributor"><strong>Jaweria:</strong> & Model Training – oversaw the project, trained and evaluated models.</div>
    <div class="contributor"><strong>Bushra:</strong> EDA & Visualization – analyzed trends and created visualizations.</div>
    <div class="contributor"><strong>Siddique:</strong> Feature Engineering – created technical features aligned with model requirements.</div>
    <div class="contributor"><strong>Hamayl:</strong> Evaluation, Reporting & Presentation – evaluated models, prepared visualizations, reports, and demo video.</div>
</div>
<br>
<h2>Usage</h2>
<p style="text-align:center;">
Clone the repository and run Jupyter notebooks:
<pre>
git clone &lt;repository_url&gt;
cd stock-price-trend-prediction
jupyter notebook
</pre>
</p>

<br>
<h2>Listen & Contact</h2>
<p class="contact">
For queries, feedback, or collaboration:<br>
Email: <strong>hamaylzahid@gmail.com</strong><br>
GitHub: <a href="https://github.com/hamaylzahid" target="_blank">github.com/hamaylzahid</a>
</p>
<br>

<h2>License</h2>
<br>
<div style="text-align:center;">
    <img src="https://img.shields.io/badge/License-MIT-brightgreen" alt="License Badge"><br><br>
    This project is licensed under the <strong>MIT License</strong>. You are free to use, modify, and distribute this project, provided proper attribution is given.
</div>
<br>

</body>
</html>
