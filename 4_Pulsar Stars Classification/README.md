# Pulsar Stars Classification

**EN** · [RU](#классификация-пульсаров)

Binary classification of radio signals from the HTRU2 survey (17,898 candidates, 8 statistical features): is the source a pulsar or noise/interference?

**What was done**
- EDA: data quality check, profiling, correlation analysis, feature importance (Decision Tree, Random Forest).
- Preprocessing: train/test split, MinMax scaling.
- Compared 6 classifiers: Decision Tree, Random Forest, SVM (linear and polynomial kernels), KNN, Logistic Regression, evaluated with accuracy and confusion matrices.
- Built a multilayer neural network in Keras as a benchmark.

**Result:** Random Forest performed best, with **98.3%** test accuracy. The neural network reached about 97%.

**Stack:** Python, pandas, NumPy, scikit-learn, Keras, seaborn, matplotlib, pandas-profiling.

---

## Классификация пульсаров

[EN](#pulsar-stars-classification) · **RU**

Бинарная классификация радиосигналов обзора HTRU2 (17 898 кандидатов, 8 статистических признаков): это пульсар или шум/помеха?

**Что сделано**
- EDA: проверка качества данных, профилирование, корреляционный анализ, важность признаков (Decision Tree, Random Forest).
- Предобработка: разбиение на обучающую и тестовую выборки, масштабирование MinMax.
- Сравнение 6 классификаторов: Decision Tree, Random Forest, SVM (линейное и полиномиальное ядро), KNN, логистическая регрессия; оценка по accuracy и матрицам ошибок.
- Для сравнения построена многослойная нейросеть на Keras.

**Результат:** лучшая модель — Random Forest, **98,3%** accuracy на тестовой выборке. Нейросеть показала около 97%.

**Стек:** Python, pandas, NumPy, scikit-learn, Keras, seaborn, matplotlib, pandas-profiling.

<a href="Pulsar Stars Classification_ENG.ipynb" style="text-decoration:none;">
  <div style="display:inline-block; padding:10px 20px; font-size:18px; font-weight:bold; color:white; background-color:#007bff; border-radius:5px;">
    Go to the project / Перейти к проекту
  </div>
</a>
