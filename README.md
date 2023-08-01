# Stock Prediction Streamlit app
Check out the website [here](http://103-241-65-61.cloud-xip.com:8501/).
Check out the full DagsHub repository [here](https://dagshub.com/somesh.d84/StockPrediction)

App predicts if tomorrow the stock price will go UP or DOWN. It uses an end-to-end MLops pipeline using ZenML.

## Features

- Web interface for stock symbol input. 
- Fetching historical stock data. Data taken from realtime AlphaVantage API.
- Training machine learning models to predict future stock prices
- Logging experiments with MLflow
- Packaging models and deploying via MlFlow
- Orchestrating pipeline with ZenML

## Usage

To run the app locally:

```bash
streamlit run streamlit_app.py
```

Input a stock symbol to fetch data. The app will run the entire ZenML pipeline for each stock which trains a model, evaluates it, and registers the best model.


## Pipeline Architecture

![architecture diagram](https://dagshub.com/somesh.d84/StockPrediction/raw/MLflowDeployer/StockPredArch.png)

- Web frontend: Streamlit
- ML Pipeline: ZenML
- Experiment tracking: MLflow 
- Model packaging: Docker
- Container registry: DockerHub

## Example ZenML deploy pipeline run
![Zenml Deploy pipeline visualisation](https://dagshub.com/somesh.d84/StockPrediction/raw/MLflowDeployer/ZenmlDepPipe.png)
