# Avocado Price Prediction

**EN** · [RU](#прогнозирование-цен-на-авокадо)

Regression on historical avocado sales data (18,249 weekly records for 2015–2018, 54 regions): predict the average price of an avocado from sales volumes, type, region and season.

**What was done**
- EDA: data quality check, price analysis by region, type (conventional/organic), year and season, correlation of features with price.
- Feature engineering: regions geocoded with geopy (Nominatim) and grouped by country, dates converted to seasons, One-Hot Encoding of the categorical features (country, type, year, season), missing values filled with the mean.
- Preprocessing: train/test split (80/20), MinMax scaling.
- Compared 6 regressors: Linear Regression, Decision Tree, Gradient Boosting, Random Forest, KNN, SVR, evaluated with MAE, MSE and R².
- Built a multilayer neural network in Keras as a benchmark.

**Result:** Random Forest performed best, with **R² = 0.89** on the test set and MAE of about **$0.09** (about 6% of the average price of $1.41). Decision Tree came second (R² = 0.76). The neural network trained stably, but its error (MSE of about 0.06 on the validation split) was well behind Random Forest (0.017).

**Stack:** Python, pandas, NumPy, scikit-learn, Keras, geopy, seaborn, matplotlib.

---

## Прогнозирование цен на авокадо

[EN](#avocado-price-prediction) · **RU**

Регрессия на исторических данных о продажах авокадо (18 249 недельных записей за 2015–2018 годы, 54 региона): прогноз средней цены авокадо по объёмам продаж, типу, региону и сезону.

**Что сделано**
- EDA: проверка качества данных, анализ цены по регионам, типу (обычные/органические), годам и сезонам, корреляция признаков с ценой.
- Подготовка признаков: регионы геокодированы через geopy (Nominatim) и сгруппированы по странам, даты преобразованы в сезоны, категориальные признаки (страна, тип, год, сезон) закодированы через One-Hot Encoding, пропуски заполнены средним.
- Предобработка: разбиение на обучающую и тестовую выборки (80/20), масштабирование MinMax.
- Сравнение 6 регрессоров: линейная регрессия, Decision Tree, Gradient Boosting, Random Forest, KNN, SVR; оценка по MAE, MSE и R².
- Для сравнения построена многослойная нейросеть на Keras.

**Результат:** лучшая модель - Random Forest, **R² = 0,89** на тестовой выборке и MAE около **$0,09** (примерно 6% от средней цены $1,41). На втором месте Decision Tree (R² = 0,76). Нейросеть обучалась стабильно, но по ошибке (MSE около 0,06 на валидационной выборке) заметно уступила Random Forest (0,017).

**Стек:** Python, pandas, NumPy, scikit-learn, Keras, geopy, seaborn, matplotlib.

<a href="Avocado price prediction_ENG.ipynb" style="text-decoration:none;">
  <div style="display:inline-block; padding:10px 20px; font-size:18px; font-weight:bold; color:white; background-color:#007bff; border-radius:5px;">
    Go to the project / Перейти к проекту
  </div>
</a>
