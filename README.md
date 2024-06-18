
# Stock Price Prediction with Sentiment Analysis (Hybrid Model)

## Description
This project combines web scraping, sentiment analysis, and LSTM neural networks to predict stock prices based on news sentiment. It fetches financial news headlines from Finviz, analyzes sentiment using VADER (Valence Aware Dictionary and sEntiment Reasoner), fetches historical stock data from Yahoo Finance, and trains an LSTM model for prediction.

The workflow includes:
- **Fetching News**: Retrieves news headlines related to a specified stock ticker.
- **Sentiment Analysis**: Analyzes sentiment (positive or negative) of each headline using VADER.
- **Historical Data Fetching**: Retrieves historical stock data including daily closing prices.
- **LSTM Model Training**: Prepares data for LSTM training by scaling and creating sequences of historical closing prices.
- **Prediction**: Trains an LSTM model to predict future stock prices based on historical data and sentiment scores.

## Dependencies
- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `yfinance`
  - `nltk`
  - `beautifulsoup4`
  - `keras`
  - `scikit-learn`

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/stock-price-prediction.git
   cd stock-price-prediction
   ```
   
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   
3. Ensure NLTK data is downloaded (for sentiment analysis):
   ```bash
   python -m nltk.downloader vader_lexicon
   ```
   
4. Run the main script with a specified stock ticker (e.g., 'AAPL'):
   ```bash
   python main.py AAPL
   ```

## Usage
- Replace `'AAPL'` with any valid stock ticker symbol (e.g., 'GOOG', 'MSFT', 'AMZN') to analyze news and predict stock prices for different companies.
- The program will fetch recent news headlines, analyze their sentiment, fetch historical stock data, train an LSTM model, and print out sentiment scores along with news headlines.

## Example Output
After running the script for a stock ticker like 'AAPL', the output will display news headlines along with their sentiment scores and proceed to train an LSTM model based on historical data.

## Potential Enhancements
- Implement error handling for cases where no news is found or errors occur during web scraping.
- Optimize performance by parallelizing news fetching and sentiment analysis tasks.
- Experiment with different LSTM architectures, hyperparameters, and additional features for improved stock price prediction accuracy.
- Visualize sentiment trends over time and compare predicted vs. actual stock prices for deeper analysis.

---

This README file provides a comprehensive overview of your project, outlining its functionality, dependencies, setup instructions, usage guidelines, and suggestions for further enhancements. Adjust the sections and details as per your specific implementation and project requirements.
