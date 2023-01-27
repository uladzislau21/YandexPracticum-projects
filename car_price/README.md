# Предсказание стоимости автомобилей / Cars' price prediction

## Цель проекта / Project goal
Построить модель машинного обучения, которая по различным характеристикам автомобиля будет предсказывать его цену. Данная модель будет использоваться сервисом по продаже автомобилей.

При оценке модели машинного обучения необходимо следующие характеристики:

- качество предсказания,
- скорость предсказания,
- время обучения.

Build a machine learning model that will predict car price based on various characteristics. This model will be used by the car sales service.

When evaluating a machine learning model, the following characteristics are required:

- the quality of the prediction,
- prediction speed,
- studying time.

## Проделанные шаги / Workflow

### Данные / Data
Исторические данные содержат различные характеристики автомобиля. Например, тип кузова, тип коробки передач, мощность, модель, пробег, год выпуска, и т.д. Целевая переменная - цена автомобиля.

Historical data contains various vehicle characteristics. For example, vehicle type, gearbox type, power, model, mileage, year of manufacture, etc. The target variable is the price of the car.

### Подготовка данных + ИАД / Data preparation + EDA
На данном этапе изменили названия колонок, тип переменных, заполнили пропуски, проанализировали аномальные значения, закодировали категориальные переменные, и стандартизировали численные переменные.

At this stage, we changed the column names, the type of variables, filled in the missing values, analyzed the outliers, encoded the categorical variables, and standardized the numerical variables.

### Обучение модели / Model training
Выбрали признаки для обучения и разбили на обучающую и тестовую выборки. Использовали простую `линейную регрессию`, `дерево решений`, `случайный лес`, и `градиентный бустинг`. Все модели (кроме линейной регрессии) были построены в двух вариантах: базовая модель и модель с оптимизированными гиперпараметрами. Для оптимизации параметров использовали бибилиотеку `hyperopt`.

We selected features for training and divided data into training and test sets. We used `linear regression`, `decision tree`, `random forest`, and `gradient boosting`. All models (except linear regression) were built in two versions: a base model and a model with optimized hyperparameters. The `hyperopt` library was used to optimize the parameters.

### Анализ моделей / Model evaluation
Проверили время обучения и предсказания всех моделей, а также метрику `RMSE` для валидационной и тестовой выборок и процентную разницу между ними.

We checked the training and prediction times of all models, as well as the `RMSE` metric for the validation and test sets and the percentage difference between them.