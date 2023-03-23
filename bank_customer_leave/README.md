# Предсказание оттока клиентов из банка / Predicting the churn of customers from the bank

## Цель проекта / Project goal
Построить модель машинного обучения для предсказания ухода клиентов из банка, которая будет иметь F1-score не меньше 0.59.

Develop machine learning model that predicts whether a bank customer would leave. The model has to achieve F1-score not less than 0.59.

## Проделанные шаги / Workflow

### Данные / Data
Данные были взяты с Kaggle https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling.

Data source: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling.

### Изучение данных / Data exploration
Были проверены пропуски, дубликаты, и аномальные значения, а также дисбаланс в целевой переменной. Также был построен парный график для изучения корреляций между переменными.

Missing values, duplicates, and anomal values were checked. A pair plot was also constructed to examine correlations between variables.

### Предобработка данных / Data preprocessing
Были удалены лишние колонки и колонка с пропусками, категориальные данные были закодированы, данные были стандартизированы и разделены на тренировочный, тестовый и валидационный датасеты.

Extra columns and a column with missing values were removed, categorical data were encoded, the data was standardized and divided into training, test and validation datasets.

### Построение модели / Model training
Было построено несколько моделей классификации (логистическая регрессия, дерево решений, и случайный лес) в различных вариациях. Сначала были построены модели без оптимизации гиперпараметров на данных с дисбалансом в целевой переменной. Затем эти же модели были оптимизированы и обучены на несбалансированных данных. Далее, классы в целевой переменной были сбалансированны и те же модели были построены в двух вариациях: с оптимизацией и без оптимизации гиперпараметров. Две лучшие модели были выбраны для проверки на тестовых данных. В качестве финальной модели был выбран оптимизированный случайный лес, обученный на данных без дисбаланса классов (upsampling).

Several classification models were built (logistic regression, decision tree, and random forest) in various variations. First, models were built without hyperparameter optimization on data with an imbalance in the target variable. These same models were then optimized and trained on unbalanced data. Further, the classes in the target variable were balanced and the same models were built in two variations: with and without optimization of hyperparameters. The two best models were chosen to be tested against the test data. An optimized random forest trained on data without class imbalance (upsampling) was chosen as the final model.
