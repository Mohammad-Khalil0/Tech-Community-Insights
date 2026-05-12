# COSC482 Tech Community Insights

Data Science and Web Scraping course project for `COSC482` at `RHU` in `Fall 2025`. This project collects post data from Hacker News and Lobsters, cleans and combines the datasets, generates visual analytics, and presents the results through an interactive Streamlit dashboard and static report exports.

## Project Overview

The project studies how two tech communities behave by comparing:

- post popularity
- comment activity
- engagement patterns by time
- title length and engagement
- sentiment in post titles
- topic trends using NLP

## Data Sources

- Hacker News API
- Lobsters JSON API

## Main Features

- Automated scraping from Hacker News and Lobsters
- Data cleaning and normalization with Pandas
- Comparative analysis across both platforms
- NLP-based semantic search in the Streamlit dashboard
- Visual reports exported to the `visualizations/` folder
- GitHub Actions workflow for scheduled refresh and analysis

## Project Structure

```text
.
|-- scraper_hn.py          # Scrapes top Hacker News posts
|-- Lobste.py              # Scrapes Lobsters posts
|-- cleaner.py             # Cleans and standardizes raw data
|-- analysis.py            # Generates analysis outputs and charts
|-- dashboard.py           # Streamlit dashboard
|-- index.html             # Static page for exported visualizations
|-- raw_data/              # Raw scraped CSV files
|-- clean_data/            # Cleaned CSV files
|-- visualizations/        # Generated charts and analysis report
`-- .github/workflows/     # Automation workflow
```

## How To Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Scrape fresh data

```bash
python Lobste.py
python scraper_hn.py
```

### 3. Clean the datasets

```bash
python cleaner.py
```

### 4. Generate analysis outputs

```bash
python analysis.py
```

### 5. Launch the interactive dashboard

```bash
streamlit run dashboard.py
```

### 6. Preview the static export page

After generating the charts, you can also preview the static report page:

```bash
python -m http.server 8000
```

Then open:

- `http://localhost:8501` for the Streamlit dashboard
- `http://localhost:8000` for the static visualization page

## Live Demo

- Streamlit demo: [Open Streamlit App](https://tech-community-insights.streamlit.app/)
- GitHub Pages demo: [Open GitHub Pages](https://mohammad-khalil0.github.io/Tech-Community-Insights/)

## Automation

The GitHub Actions workflow in `.github/workflows/main.yml` is configured to:

- run on push
- run manually
- run every 6 hours on schedule
- refresh scraped data
- regenerate cleaned datasets and visualizations

This makes the repository suitable for a continuously updated course project showcase.

## What I Learned From COSC482

Through this project, I practiced:

- collecting structured data from public APIs and websites
- handling messy real-world datasets
- cleaning and transforming data with Pandas
- comparing platforms using descriptive analytics
- building visualizations for storytelling
- applying NLP techniques such as sentiment analysis and TF-IDF search
- turning analysis into an interactive dashboard
- automating a data workflow with GitHub Actions

## Course Context

This repository was developed as part of the `COSC482 Data Science & Web Scraping` course at `Rafik Hariri University (RHU)` during the `Fall 2025` semester.

## Authors

This project was completed by `Mohammad Khalil` and teammate `Mohammad Sati`.

## Copyright

Copyright © 2026. All rights reserved.

See the [LICENSE](LICENSE) file for full terms.
