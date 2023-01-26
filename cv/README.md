# Определение возраста покупателя по фотографии / Age determination of customer from photo

## Цель проекта / Project goal
Используя нейронные сети, обучить модель предсказания возраста покупателей по фотографии. В дальнейшем внедрение такой системы в супермаркете позволит:

- рекомендовать товары покупателям с большей эффективностью,
- устранить попытки покупки несовершеннолетними алкоголя и табака.

Using neural networks, train a model for predicting the age of customers from a photo. In the future, the introduction of such a system in the supermarket will allow:

- recommend products to customers with greater efficiency,
- eliminate attempts to purchase alcohol and tobacco by minors.

## Проделанные шаги / Workflow

### Данные / Data
Данные были взяты с сайта [ChaLearn Looking at People](https://chalearnlap.cvc.uab.cat/dataset/36/description/). Данные организованы в следущую структуру: папка со всеми изображениями и датасет с двумя колонками (название файла и возраст человека на соответствующем изображении).

Data was taken from [ChaLearn Looking at People](https://chalearnlap.cvc.uab.cat/dataset/36/description/). The data is organized in the following structure: a folder with all images and a dataset with two columns (file name and age of the person in the corresponding image).

### Исследовательский анализ данных / Exploatory data analysis
На данном этапе была проверена размерность датафрэйма и проруски. 10 изображений были напечатаны на экран в виде графика. Также было проверено распределение возраста в данных.

At this stage, the dimension of the dataframe and prorusk was checked. 10 images were printed onto the screen as a graph. The distribution of age in the data was also checked.

### Обучение модели / Model training
Для достижение поставленной цели использовали сверточную нейронную сеть `ResNet50`. Модель была обучена в отдельном GPU-тренажере. Код в ноутбуке выведен как текстовая ячейка. Также представлен вывод тренажера во ремя обучения модели.

To achieve this goal, the `ResNet50` convolutional neural network was used. The model was trained in a separate GPU simulator. The code in the notebook is displayed as a text cell. The output of the simulator during model training is also presented.

### Анализ модели / Model evaluation
