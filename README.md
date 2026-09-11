# Seattle Airbnb Data Analytics & Business Insights

An end-to-end data analytics project exploring Seattle Airbnb listing pricing, market occupancy, host performance metrics, and property characteristics using Python and Tableau.

---

## Key Business Highlights & Executive Summary

Across **3,730 total listings** analyzed in Seattle, the market reflects an average daily rate (ADR) of **$128.47** (median: $100.00) and an estimated occupancy rate of **32.93%**.

### Core Findings & Strategic Recommendations
- **Capacity Impact:** Guest capacity is the primary driver of listing price (**65.27% correlation**). Expanding listing capacity directly yields higher rates.
- **Cancellation Policy Premium:** Listings with strict cancellation policies command an average price premium of **$45.30** compared to flexible options.
- **Superhost Evaluation:** Superhost status yields only a modest **$3.56 price premium** ($131.31 vs. $127.75 for standard hosts), indicating pricing power relies more on location and size than status badges.
- **Top Revenue Markets:** Portfolio revenue is heavily concentrated in high-volume neighborhoods like **Capitol Hill ($5.86M)** and **Belltown ($4.72M)**.

**[Read Full Executive Summary & Business Recommendations](docs/executive-summary_and_business_recommendations.md)**

---

## Interactive Dashboard

View the full interactive visualization dashboard on Tableau Public:  
👉 **[https://public.tableau.com/views/airbnbanalytics_17891255294750/Executive?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link]**

---

## Tech Stack & Tools

- **Language:** Python 3.x
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Visualization:** Tableau Public
- **Environment:** Jupyter Notebook / Google Colab

---

## Data Preprocessing & Cleaning Pipeline

1. **Feature Selection:** Screened and narrowed 90+ raw features down to core analytical metrics.
2. **Currency Parsing:** Cleaned and formatted raw string currencies (`$1,250.00`) across `price`, `cleaning_fee`, and `security_deposit` to standard numeric `float64`.
3. **Percentage Normalization:** Cast string percentages (`host_response_rate`, `host_acceptance_rate`) to decimal floats (`0.0`–`1.0`).
4. **Boolean Encoding:** Transformed 't'/'f' string flags into binary booleans (`host_is_superhost`, `instant_bookable`).
5. **Outlier Treatment:** Applied IQR-based statistical techniques to isolate and evaluate extreme price variations.

---

## Repository Structure

```text
├── data/
│   └── listings.csv                                    # Raw Airbnb dataset
├── docs/
│   └── executive-summary_and_business_recommendations.md # Strategic Business Report
├── images/
|    └── airbnb analytics 1.png #Exective Dashboard
|    └── airbnb analytics 2.png #Price Drivers
|    └── airbnb analytics 3.png #Statistical Analysis
├── notebooks/
│   └── airbnb_data_cleaning_and_preprocessing.ipynb    # Data Cleaning & Preprocessing
|   └── airbnb_eda_and_hypothesis_testing.ipynb         # EDA & Hypothesis Testing
├── README.md                                           # Repository Overview
└── requirements.txt                                    # Dependencies
