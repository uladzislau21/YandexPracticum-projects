# Рекомендация тарифов / Tariff recommendation

## Цель проекта / Project goal
Построить модель иашинного обучения (классификатор) для рекомендации нового тарифа клиентам телеком компании.

To build a machine learning model (classifier) to recommend a new tariff to the telecom company's customers.

## Проделанные шаги / Workflow

### Данные / Data
Использовали данные об активности клиентов, которые уже перешли на новые тарифы.

We used data on the activity of customers who have already switched to new tariffs.

### Изучение данных / Data
Провели исследовательский анализ данных.

Performed EDA of the data.

### Подготовка данных / Data preprocessing
Изменили типы у некоторых переменных, а также разбили данные на тренировочный, тестовый, и валидационный наборы.

We changed the types of some variables, and also split the data into training, test, and validation sets.

### Построение моделей и их валидация / Training and validation of models
Построили модели логистической регрессии, дерева решений, и случайного леса. Проверили их **accuracy** на валидационной выборке. Затем оптимизировали гиперапараметры случайного леса и дерева решений.

We created models of logistic regression, decision tree, and random forest. Checked them **accuracy** on the validation set. Then the hyperparameters of the random forest and decision tree were optimized.

### Проверка модели на тестовой выборке / Model assesment on test set
Выбрали оптимизированную модель случайного леса для проверки на тестовой выборке. Финальное значение точности 0.83.

We chose an optimized random forest model for testing on a test set. The final accuracy value is 0.83.
