# Выбор локации для скважины / Choosing a location for an oil well

## Цель проекта / Project goal
Построить модель машинного обучения для предсказания прибыли и убытков в трёх регионах нефтедобычи.

To build a machine learning model for profit and loss prediction in three regions of oil mining.

## Проделанные шаги / Workflow

### Данные / Data
Данные представляют собой параметры скважины с объемом запасов нефти в каждой из них.

The data are well parameters with the volume of oil reserves in each of them.

### Изучение данных / Data
Провели исследовательский анализ данных. Никакой предобработки даных не понадобилось.

Conducted exploratory data analysis. No data preprocessing was required.

### Построение модели и предсказание / Model training and prediction
Построили 3 модели линейной регрессии. Предсказали запасы сырья, используя построенные модели.

We built 3 linear regression models. We predicted the stocks of raw materials using the built models.

### Расчет прибыли и рисков / Profit and risk assesment
Далее рассчитали объем сырья, необходимый для безубыточной работы. Далее написали функцию для расчета прибыли, которая на вход принимает целевые значения запасов нефти, предсказанные запасы нефти, и количество скважин для разработки. Далее, используя эту функцию и технику **Bootstrap** рассчитали прибыль и риски.

Next, we calculated the volume of raw materials required for break-even operation. Next, we wrote a function for calculating the profit, which takes as input the target values of oil reserves, predicted oil reserves, and the number of wells for development. Next, using this function and the **Bootstrap** technique, we calculated the profit and risk.