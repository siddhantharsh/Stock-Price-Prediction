# Stock Price Prediction Using LSTM

A deep learning project that uses Long Short-Term Memory (LSTM) neural networks to predict stock prices. The project includes both a Jupyter notebook for analysis and a Flask web application for real-time predictions.

## Developer
- **Name:** Siddhant Harsh
- **Email:** siddhant101213@gmail.com

## Features
- Historical stock data visualization using candlestick charts
- Moving averages (100-day and 200-day) analysis
- Exponential moving averages visualization
- LSTM-based price prediction model
- Interactive web interface for real-time predictions
- Support for multiple stock exchanges (NSE, BSE, NYSE, NASDAQ)

## Supported Stock Symbols
- US Stocks (e.g., AAPL, MSFT, GOOGL, AMZN, TSLA)
- Indian NSE Stocks (add .NS - e.g., RELIANCE.NS, TCS.NS, HDFCBANK.NS)
- Indian BSE Stocks (add .BO - e.g., RELIANCE.BO, TCS.BO)

## Technical Stack
- Python 3.x
- TensorFlow/Keras for LSTM model
- Flask for web application
- Pandas for data manipulation
- yfinance for stock data retrieval
- Plotly and Matplotlib for visualization

## Installation
1. Clone the repository
2. Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```
3. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage
### Jupyter Notebook
1. Open `Stock Price Prediction .ipynb`
2. Change the stock symbol in the notebook:
```python
stock = "YOUR_STOCK_SYMBOL"  # e.g., "AAPL" for Apple, "RELIANCE.NS" for Reliance NSE
```
3. Run all cells to:
   - Fetch historical data
   - Visualize trends
   - Train the LSTM model
   - Generate predictions

### Web Application
1. Run the Flask app:
```bash
python app.py
```
2. Open `http://localhost:5000` in your browser
3. Enter a stock symbol and get predictions

## Model Architecture
- LSTM neural network with multiple layers
- Input shape: 100 time steps (days) of price data
- Layer configuration:
  - LSTM (50 units) + Dropout (0.2)
  - LSTM (60 units) + Dropout (0.3)
  - LSTM (80 units) + Dropout (0.4)
  - LSTM (120 units) + Dropout (0.5)
  - Dense (1 unit) for prediction

## Performance Metrics
- Training-Testing Split: 70%-30%
- Loss Function: Mean Squared Error
- Optimizer: Adam
- Visualization: Actual vs Predicted prices

## Files Description
- `Stock Price Prediction .ipynb`: Main Jupyter notebook with analysis and model training
- `app.py`: Flask web application
- `stock_dl_model.h5`: Trained model file
- `static/`: CSS and image files
- `templates/`: HTML templates
- `powergrid.csv`: Sample stock data

## License
This project is open source and available for educational and research purposes.

## Contributing
Feel free to contribute to this project by submitting pull requests or reporting issues.