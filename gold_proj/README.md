# Восстановление золота из руды / Recovery of gold from ore

## Цель проекта / Project goal
Для промышленной компании по добыче золота построить модель машинного обучения для предсказания восстановления золота из руды. Данная модель поможет избежать запуска убыточных проектов.

For an industrial gold mining company, build a machine learning model to predict the recovery of gold from ore. This model will help to avoid launching unprofitable projects.

## Проделанные шаги / Workflow

### Данные / Data
От копмании получили тренировочные и тестовые данные.

We received training and test data from the company.

### Изучение данных / Data
На данном этапе познакомились с данными, изучили технологический процесс добычи золота, а также проверили правильность расчёта коэффициента восстановления.

At this stage, we got acquainted with the data, studied the technological process of gold mining, and also checked the correctness of the calculation of the recovery factor.

### Предобработка данных / Data preprocessing
Тестовые данные не содержали некоторых признаков, имеющихся в тренировочном наборе. Поэтому, изучили и удалили их. Также в тестовую выбрку был добавлен целевой признак. Далее заполнили пропуски. Для этого брали среднее двух соседних значений так как данные индексируются временем и соседние точки данных очень похожи.

The test data did not contain some of the features found in the training set. Therefore, studied and removed them. Also, a target feature was added to the test sample. Then they filled in the gaps. To do this, we took the average of two neighboring values, since the data is indexed by time and neighboring data points are very similar.

### Исследовательский анализ данных / Exploatory data analysis
С использованием библиотеки `dtale` изучили взаимосвязи в данных. Напрмиер, была построена тепловая карта корреляций между переменными. Далее построили различные графики, отражающие изменение концентрации металов на различных этапах очистки. Также, мы сравненили распределения размеров гранул сырья на обучающей и тестовой выборках. Наконец, исследовали суммарную концентрацию всех веществ на разных стадиях: в сырье, в черновом и финальном концентратах.

Using the `dtale` library, we studied the relationships in the data. For example, a heat map of correlations between variables was built. Next, various graphs were constructed, reflecting the change in the concentration of metals at various stages of purification. Also, we compared the size distributions of raw material granules on the training and test samples. Finally, we studied the total concentration of all substances at different stages: in raw materials, in roughing and final concentrates.

### Построение модели / Model training
В этом проекте в качестве метрики использовали кастомную функцию `sMAPE` (англ. Symmetric Mean Absolute Percentage Error, «симметричное среднее абсолютное процентное отклонение»). Использование именно этой функции позволило учесть масштаб целевого признака и предсказания.
Сначала построили базовую модель линейной регрессии. Затем обучили LASSO-регрессию, чтобы учесть мультиколлинеарность в данных, а также отобрать важные признаки. Для сравнения обучили регрессионный случайный лес.
Отличий между LASSO-регрессией и случайным лесом не обнаружили, поэтому для проверки модели на тестовых данных использовали LASSO-регрессию с отобранными признаками.

In this project, the custom function `sMAPE` (Symmetric Mean Absolute Percentage Error) was used as a metric. The use of this particular function made it possible to take into account the scale of the target feature and prediction. First, a basic linear regression model was built. Then we trained LASSO regression to take into account multicollinearity in the data, as well as to select important features. For comparison, a regression random forest was trained. No differences were found between LASSO regression and random forest, so LASSO regression with selected features was used to test the model on test data.
