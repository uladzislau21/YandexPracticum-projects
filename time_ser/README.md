# Прогнозирование заказов такси / Taxi orders prediction

## Цель проекта / Project goal
Построить модель машинного обучения для предсказания количества заказов такси на следующий час и добиться метрики RMSE не больше 48.

Build a machine learning model to predict the number of taxi orders for the next hour and achieve an RMSE metric of no more than 48.

## Проделанные шаги / Workflow

### Данные / Data
Данные содержат количество заказов такси каждые 10 минут за полгода.

The data contains the number of taxi orders every 10 minutes for six months.


### Изучение данных / EDA
Суммировали данные по одному часу. Далее провели исследовательский анализ данных. Проверили распределение заказов в час. Визуализировали тренд, сезонность, и остатки.

Summarized data for one hour. Next, an exploratory analysis of the data was carried out. Checked the distribution of orders per hour. Visualized the trend, seasonality, and residuals.


### Предобработка данных / Data preprocessing
Создали признаки для обучения модели. Целевой перменной сделали разницу ряда. Также добавили в признаки день недели, отставание, и скользящее среднее. Разбили данные на валидационную, тренировочную, и тестовую выборки.

Created features for training the model. The target variable was made the difference of the series. We also added the day of the week, lag, and moving average to the features. The data was divided into validation, training, and test sets.


### Построение модели / Model training
Построили базовые модели: предсказание средним или предыдущим из ряда значением. Затем подобрали гиперпараметры для генерации признаков **max_lag** и **rolling_mean_window**. Оценили качество базовых моделей на данных, полученных с оптимизированными гиперпараметрами. Далее обучили линейную регрессию и **ARIMA** и оптимизировали эти модели. Для проверки модели на тестовой выборке выбрали оптимизированную линейную регрессию. Модель показала метрику ниже пороговой.

We built basic models: prediction by the average or the previous value from the series. Then hyperparameters were selected to generate features **max_lag** and **rolling_mean_window**. We assessed the quality of the base models on data obtained with optimized hyperparameters. Next, we trained linear regression and **ARIMA** and optimized these models. To test the model on a test sample, we chose an optimized linear regression. The model showed a metric below the threshold.
