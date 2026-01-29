# 🪙 Automated Crypto Data Runner

An automated data pipeline built with **Python** that connects to the **CoinMarketCap API** to fetch, normalize, and store real-time cryptocurrency market data. This project mimics a real-world **ETL (Extract, Transform, Load)** process, designed to monitor market volatility for top cryptocurrencies.

## 📌 Project Overview

This script runs a continuous loop to query live market data, transforming raw nested JSON responses into a structured Pandas DataFrame. It is designed to act as a data ingestion engine for downstream analysis or visualization dashboards.

**Key Objectives:**

* **Automate Data Ingestion:** Remove manual CSV downloads by engineering a script that pulls fresh data at set intervals.
* **Handle API Complexity:** Manage secure headers, session authentication, and query parameters.
* **Data Transformation:** Flatten complex nested JSON structures (e.g., `quote.USD.price`) into a clean tabular format.

## 🚀 Features

* **Live API Connection:** Utilizes `requests` and `Session` to maintain a persistent, secure connection to the CoinMarketCap Professional API.
* **Robust Error Handling:** Includes `try/except` blocks to gracefully manage connection timeouts, rate limits, and redirect errors.
* **Data Normalization:** Uses `pandas.json_normalize` to convert raw API outputs into a ready-to-analyze DataFrame.
* **Automated Scheduler:** Features a custom `api_runner` loop that fetches data every 60 seconds (configurable), appending it to a master dataset with precise timestamps.

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Libraries:**
* `pandas` (Data manipulation & storage)
* `requests` (HTTP requests)
* `json` (Data parsing)
* `os` & `time` (System operations & scheduling)


* **Source:** [CoinMarketCap API](https://coinmarketcap.com/api/)

## ⚙️ Installation & Usage

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/crypto-api-runner.git
cd crypto-api-runner

```


2. **Install Dependencies**
```bash
pip install pandas requests

```


3. **Get an API Key**
* Sign up for a free API key at [CoinMarketCap Developer Platform](https://coinmarketcap.com/api/).
* Replace `'YOUR_API_KEY'` in the script with your actual key.


4. **Run the Script**
Open `Crypto_API.ipynb` in Jupyter Notebook or VS Code and execute the cells. The `api_runner` loop is set to run for a defined number of iterations.


---

*If you find this project useful, please ⭐ the repository!*
