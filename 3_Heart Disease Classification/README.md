# Heart Disease Classification

**EN** · [RU](#классификация-сердечных-заболеваний)

Binary classification of patients from the UCI Heart Disease dataset (303 patients, 13 clinical features): does the patient have heart disease?

**What was done**
- EDA: data quality check, profiling, correlation analysis. The features most correlated with the target are chest pain type (`cp`), maximum heart rate (`thalach`) and ST segment slope (`slope`).
- Feature engineering: age binned into 5 groups, One-Hot Encoding of the categorical features (`cp`, `restecg`, `slope`, `thal`, `ca`), and removal of 2 records with an undocumented `thal` value.
- Preprocessing: train/test split (70/30), MinMax scaling.
- Compared 6 classifiers: Decision Tree, Random Forest, SVM (linear and polynomial kernels), KNN, Logistic Regression, evaluated with accuracy and confusion matrices.
- Built a multilayer neural network in Keras as a benchmark.

**Result:** Logistic Regression performed best, with **87.9%** test accuracy, followed by SVM with a polynomial kernel (84.6%). The neural network reached about 88% on the validation split, but overfitted and did not beat the classical models.

**Stack:** Python, pandas, NumPy, scikit-learn, Keras, seaborn, matplotlib, pandas-profiling.

---

## Классификация сердечных заболеваний

[EN](#heart-disease-classification) · **RU**

Бинарная классификация пациентов из набора данных UCI Heart Disease (303 пациента, 13 клинических признаков): есть ли у пациента заболевание сердца?

**Что сделано**
- EDA: проверка качества данных, профилирование, корреляционный анализ. Сильнее всего с целевой переменной связаны тип боли в груди (`cp`), максимальная частота пульса (`thalach`) и наклон сегмента ST (`slope`).
- Подготовка признаков: возраст разбит на 5 групп, категориальные признаки (`cp`, `restecg`, `slope`, `thal`, `ca`) закодированы через One-Hot Encoding, удалены 2 записи с недокументированным значением `thal`.
- Предобработка: разбиение на обучающую и тестовую выборки (70/30), масштабирование MinMax.
- Сравнение 6 классификаторов: Decision Tree, Random Forest, SVM (линейное и полиномиальное ядро), KNN, логистическая регрессия; оценка по accuracy и матрицам ошибок.
- Для сравнения построена многослойная нейросеть на Keras.

**Результат:** лучшая модель - логистическая регрессия, **87,9%** accuracy на тестовой выборке, на втором месте SVM с полиномиальным ядром (84,6%). Нейросеть показала около 88% на валидационной выборке, но переобучилась и не превзошла классические модели.

**Стек:** Python, pandas, NumPy, scikit-learn, Keras, seaborn, matplotlib, pandas-profiling.

<a href="Heart Disease Classification_ENG.ipynb" style="text-decoration:none;">
  <div style="display:inline-block; padding:10px 20px; font-size:18px; font-weight:bold; color:white; background-color:#007bff; border-radius:5px;">
    Go to the project / Перейти к проекту
  </div>
</a>
