# Musical Preferences

**EN** · [RU](#музыкальные-предпочтения)

Binary classification on a Kaggle competition dataset: will the user like 👍 or dislike 👎 a song, based on their listening history? The dataset has 965 tracks (665 labelled for training, 300 for the Kaggle test set) and 17 features: artists, genres, album, label, release year, key, tempo, vocals, country, energy, danceability, happiness and others.

The main focus of the project is the data processing workflow: a mostly categorical dataset with multi-value fields (`Artist1|Artist2`) was turned step by step into a feature set a model can use.

**What was done**
- EDA: data profiling (pandas-profiling), missing-value analysis (missingno), feature descriptions loaded from a YAML file.
- Data cleaning: dropped the ID and the columns with mostly missing values (`Version`, `Album_type`), filled the remaining gaps.
- Feature engineering, with a separate approach for each feature:
  - **Artists, Labels:** grouped by how often the artist or label appears in the dataset, then One-Hot Encoded.
  - **Genres, Album:** multi-value fields expanded into one-hot vectors, rare values removed, then reduced to 2 dimensions with **t-SNE**.
  - **Key:** split into two features, the tonic (A–G, ♯/♭) and the mode (major/minor). The encoding was chosen after consulting a professional musician.
  - **Release year:** grouped into decades.
  - **Vocals, Country:** multi-value fields turned into binary features.
  - **Duration:** converted from milliseconds to seconds.
- Modelling: 6 classifiers (Decision Tree, Random Forest, SVM, KNN, Logistic Regression with ElasticNet, CatBoost), tuned with GridSearchCV and ShuffleSplit cross-validation, and combined in a hard-voting ensemble (VotingClassifier).
- Predictions submitted to Kaggle.

**Result:** Public Score **0.667** (66.7% of test tracks classified correctly). Possible next steps: deeper feature engineering, scaling the numeric features for distance-based models, and dimensionality reduction with PCA.

**Stack:** Python, pandas, NumPy, scikit-learn, CatBoost, t-SNE, pandas-profiling, missingno, seaborn, matplotlib, plotly.

Kaggle notebook: [musicpreferments-ivanko](https://www.kaggle.com/code/sanbeimailru/musicpreferments-ivanko)

---

## Музыкальные предпочтения

[EN](#musical-preferences) · **RU**

Бинарная классификация на данных соревнования Kaggle: понравится 👍 или не понравится 👎 пользователю песня, исходя из истории его прослушиваний? В наборе данных 965 треков (665 размеченных для обучения и 300 для тестовой выборки Kaggle) и 17 признаков: исполнители, жанры, альбом, лейбл, год выпуска, тональность, темп, вокал, страна, энергичность, танцевальность, «позитивность» и другие.

Основной акцент проекта - процесс обработки данных: в основном категориальный набор данных с многозначными полями (`Artist1|Artist2`) шаг за шагом превращён в признаки, с которыми может работать модель.

**Что сделано**
- EDA: профилирование данных (pandas-profiling), анализ пропусков (missingno), описания признаков загружены из YAML-файла.
- Очистка данных: удалены ID и столбцы с преобладающими пропусками (`Version`, `Album_type`), заполнены оставшиеся пропуски.
- Feature engineering, для каждого признака свой подход:
  - **Исполнители, лейблы:** сгруппированы по частоте упоминаний в наборе данных, затем закодированы через One-Hot Encoding.
  - **Жанры, альбом:** многозначные поля развёрнуты в one-hot векторы, редкие значения удалены, затем размерность снижена до 2 с помощью **t-SNE**.
  - **Тональность:** разделена на два признака - тоника (A–G, ♯/♭) и лад (мажор/минор). Способ кодирования выбран после консультации с профессиональным музыкантом.
  - **Год выпуска:** сгруппирован по десятилетиям.
  - **Вокал, страна:** многозначные поля преобразованы в бинарные признаки.
  - **Длительность:** переведена из миллисекунд в секунды.
- Моделирование: 6 классификаторов (Decision Tree, Random Forest, SVM, KNN, логистическая регрессия с ElasticNet, CatBoost), подбор гиперпараметров через GridSearchCV с кросс-валидацией ShuffleSplit, объединение в ансамбль с жёстким голосованием (VotingClassifier).
- Предсказания загружены на Kaggle.

**Результат:** Public Score **0,667** (66,7% тестовых треков классифицированы верно). Возможные следующие шаги: более глубокий feature engineering, масштабирование числовых признаков для моделей, основанных на расстояниях, и снижение размерности с помощью PCA.

**Стек:** Python, pandas, NumPy, scikit-learn, CatBoost, t-SNE, pandas-profiling, missingno, seaborn, matplotlib, plotly.

Ноутбук на Kaggle: [musicpreferments-ivanko](https://www.kaggle.com/code/sanbeimailru/musicpreferments-ivanko)

<a href="Musical preferences_ENG.ipynb" style="text-decoration:none;">
  <div style="display:inline-block; padding:10px 20px; font-size:18px; font-weight:bold; color:white; background-color:#007bff; border-radius:5px;">
    Go to the project / Перейти к проекту
  </div>
</a>
