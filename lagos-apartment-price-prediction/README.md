# Lagos Apartment Price Prediction

## Overview
A machine learning project that predicts mid-market apartment prices in Lagos, Nigeria, built using real scraped property data from Kaggle. The project progresses from a simple single-feature linear regression to a full multi-feature pipeline.

## Project Structure
```
lagos-apartment-price-prediction/
├── data/
│   └── nigeria_houses.csv
├── lagos_apartment_price_prediction.ipynb
└── README.md
```

## Covered in the project
- Iterative data wrangling with a reusable `wrangle()` function
- Exploratory data analysis and visualization (Matplotlib, Seaborn, Plotly)
- Neighborhood centroid geocoding — engineering lat/lon from town names
- Linear regression and Ridge regression (scikit-learn)
- Feature encoding with `OneHotEncoder` and imputation with `SimpleImputer`
- sklearn `Pipeline` for clean, reproducible modeling
- Overfitting diagnosis and correction with Ridge regularization
- Interactive price prediction dashboard with `ipywidgets`

## Sections
| Section | Feature Used | Model |
|--------|-------------|-------|
| 1 | Bedrooms (size proxy) | Linear Regression |
| 2 | Latitude & Longitude | Linear Regression + Pipeline |
| 3 | Neighborhood | OneHotEncoder + Ridge |
| 4 | All features combined | Full Pipeline |

## Dataset
**Nigeria Houses and Prices** — Kaggle  
`abdullahiyunus/nigeria-houses-and-prices-dataset`  
Columns: `bedrooms`, `bathrooms`, `toilets`, `parking_space`, `title`, `town`, `state`, `price`

## How to Run
1. Clone the repository
2. Install dependencies:
```bash
   pip install pandas scikit-learn matplotlib seaborn plotly category_encoders ipywidgets
```
3. Place `nigeria_houses.csv` in the `data/` folder
4. Launch Jupyter Notebook:
```bash
   jupyter notebook
```
5. Open `lagos_apartment_price_prediction.ipynb` and run cells sequentially

## Results
The final Ridge regression pipeline outperforms the baseline mean-price model,
with the neighborhood feature being the strongest price signal in the Lagos
mid-market apartment segment (properties under ₦150,000,000).

## Tools & Libraries
Python · pandas · scikit-learn · Matplotlib · Seaborn · Plotly · category_encoders · ipywidgets