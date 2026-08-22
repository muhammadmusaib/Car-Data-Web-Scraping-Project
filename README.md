# 🚗 Car Data Web Scraping & Visualization Project

This project scrapes car listing data from a demo car website, cleans and structures it into a usable dataset, and generates visual insights about manufacturing countries, model years, and mileage.

## 📌 Overview

The pipeline covers the full journey from raw HTML on a website to polished charts:

1. **Scraping** — Extract car data (name, build country, year, mileage, etc.) from a demo car website.
2. **Parsing** — Use BeautifulSoup to navigate the HTML and pull out the relevant fields.
3. **Data Handling** — Load the scraped records into a pandas DataFrame, clean it, and shape it for analysis.
4. **Visualization** — Use Seaborn (for statistical plots) and Matplotlib (for fine-grained plot control) to visualize the data.

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** | Core scripting language |
| **Requests** | Fetching raw HTML pages |
| **BeautifulSoup** | Parsing HTML and extracting data |
| **Pandas** | Data cleaning, transformation, and framing |
| **Seaborn** | Statistical & styled visualizations |
| **Matplotlib** | Additional plot customization and control |

## ⚙️ Workflow

```
Demo Car Website
      │
      ▼
 requests.get()  ──►  Raw HTML
      │
      ▼
 BeautifulSoup  ──►  Extracted fields (name, country, year, mileage, ...)
      │
      ▼
 pandas.DataFrame  ──►  Cleaned & structured dataset
      │
      ▼
 seaborn / matplotlib  ──►  Charts & insights
```

## 📂 Project Structure

```
car-scraper-project/
├── scraper.py            # Scrapes data from the demo car website using requests + BeautifulSoup
├── data_cleaning.py       # Cleans and structures data using pandas
├── visualize.py           # Generates charts using seaborn + matplotlib
├── data/
│   └── cars.csv           # Final cleaned dataset
├── images/                 # Saved chart outputs
└── README.md
```

## 🚀 How to Run

1. Clone this repository
   ```bash
   git clone <your-repo-url>
   cd car-scraper-project
   ```
2. Install dependencies
   ```bash
   pip install requests beautifulsoup4 pandas seaborn matplotlib
   ```
3. Run the scraper
   ```bash
   python scraper.py
   ```
4. Generate visualizations
   ```bash
   python visualize.py
   ```

## 🔍 Key Insights

- The **United Kingdom** and **Japan** lead in the number of cars represented in the dataset.
- The **1970-79** decade has the highest concentration of cars.
- **Italian** and **German** cars tend to have the highest average mileage.
- Classic models like the **Ford Sierra Cosworth** and **Nissan 300ZX Z31** top the list for highest individual mileage.

## 🔮 Future Improvements

- Add more filters (fuel type, price range, transmission).
- Automate scraping on a schedule to keep the dataset fresh.
- Deploy an interactive dashboard (e.g., with Streamlit or Plotly Dash).
- Store scraped data in a database instead of flat files.

## 📄 License

This project is for educational/demo purposes.
