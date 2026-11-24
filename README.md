# Tesla Stock Web Scraping & Analysis

A Python project that scrapes historical Tesla (TSLA) stock data from the web, cleans it, analyzes it, and visualizes price trends.

## Overview

This project demonstrates an end-to-end data workflow:

1. **Scrape** Tesla stock data from a web page using `requests` and `BeautifulSoup`
2. **Clean & structure** the data with `pandas`
3. **Analyze** it using `numpy` (returns, moving averages, volatility)
4. **Visualize** trends with `matplotlib`

## Tech Stack

| Library | Purpose |
|---|---|
| `requests` | Fetch the web page HTML |
| `beautifulsoup4` | Parse HTML and extract table data |
| `pandas` | Build and clean the DataFrame |
| `numpy` | Numerical calculations |
| `matplotlib` | Charts and visualizations |

## Project Structure

```
Tesla-Stock-Scrap/       # Scraped and cleaned data
   └── Tesla_Stock_WebScrap.ipynb         # Optional exploration notebook
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Hassanmukhtaar/Tesla-Stock-webscraping.git
   cd Tesla-Stock-webscraping
   ```


3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

**requirements.txt**
```
requests
beautifulsoup4
pandas
numpy
matplotlib
```

## Usage

Run the scraper to fetch and save the data:

```bash
python Tesla_Stock_WebScrap.ipynb
```

## How It Works

### 1. Scraping
The scraper sends an HTTP request (with a browser-like `User-Agent` header), parses the HTML with BeautifulSoup, locates the historical price table, and extracts rows into a list.

### 2. Cleaning
With pandas, the data is converted into a DataFrame, then:
- Dates are parsed to `datetime`
- Price and volume columns are converted to numeric types
- Missing values and non-data rows (e.g., dividend rows) are removed
- Data is sorted chronologically



### 4. Visualization
Matplotlib generates:
- Closing price over time
- Closing price with moving averages
- Trading volume
- Daily returns distribution (histogram)

## Sample Output

<img width="876" height="532" alt="stockss" src="https://github.com/user-attachments/assets/71413d84-81e1-449b-a31b-9b015a4f68ec" />





## Data Source

Data is scraped from: `<https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.html>`


## Future Improvements

- Add automatic scheduled data updates
- Add forecasting models (ARIMA, LSTM)
- Build an interactive dashboard (Streamlit or Plotly Dash)
- Compare TSLA against other EV stocks

## Author

**Hassan Mukhtar**
