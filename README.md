# Predikcija cene polovnih automobila

## Opis projekta

Cilj projekta je razvoj modela mašinskog učenja koji predviđa cenu polovnog automobila na osnovu njegovih karakteristika, kao što su proizvođač, model, godina proizvodnje, kilometraža, vrsta goriva i druge osobine.

Projekat predstavlja primer primene regresionih algoritama u Python-u.

## Korišćeni alati

- Python
- Pandas i NumPy
- Matplotlib i Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Struktura projekta

```text
car-price-prediction/
├── data/
│   └── cars.csv
├── models/
│   ├── linear_regression_model.joblib
│   └── car_price_model.joblib
├── notebooks/
│   └── 01_eda.ipynb
├── src/
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── data_preprocessing.py
│   ├── model_training.py
│   ├── model_evaluation.py
│   └── model_comparison.py
├── .gitignore
├── requirements.txt
└── README.md
```

## Obrada podataka

Tokom pripreme podataka izvršeni su:

- Istraživačka analiza podataka (EDA).
- Uklanjanje dupliranih redova.
- Provera potencijalno nevalidnih vrednosti.
- Kreiranje novih karakteristika `car_age` i `mileage_per_year`.
- Popunjavanje nedostajućih vrednosti.
- Standardizacija numeričkih karakteristika.
- One-hot kodiranje kategorijskih karakteristika.

Podaci su podeljeni na trening i test skup u odnosu 80:20.

## Treniranje i evaluacija modela

Upoređena su tri regresiona algoritma:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

Za evaluaciju su korišćene metrike MAE, MSE, RMSE i R².

| Model | MAE (USD) | RMSE (USD) | R² |
|---|---:|---:|---:|
| Linear Regression | 2089.01 | 4311.73 | 0.7230 |
| Decision Tree | 1394.65 | 3794.21 | 0.7855 |
| Random Forest | 1072.86 | 2957.47 | 0.8697 |

## Najbolji model

Najbolje rezultate ostvario je **Random Forest Regressor**, ima najmanju prosečnu apsolutnu grešku i objašnjava približno 87% varijacije cena na test skupu, sa prosečnom apsolutnom greškom od približno 1073 USD.

## Preuzimanje

Kloniranje repozitorijuma:
git clone https://github.com/nevena-blagojevic/car-price-prediction.git

## Pokretanje

Za pregled istraživačke analize podataka otvoriti notebook:
`notebooks/01_eda.ipynb`

## Autor:
Nevena Blagojević