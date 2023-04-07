# Музыка больших городов / Music of Big Cities

## Цель проекта / Project goal
Изучить и сравнить поведение людей из Москвы и Санкт-Петербурга в приложении Яндекс.Музыка для проверки следующих гипотез:

- Активность пользователей двух городов отличается в зависимости от дня недели.

- Утром в понедельник и в пятницу вечером в городах преобладают разные музыкальные жанры.

- В Москве популярен поп, а в Санкт-Петербурге - рэп.

To study and to compare the activity of people from Moscow and Saint-Peterburg in Yandex.Music app to check the following hypotheses:

- Activity of users differs between cities depending on the day of the week.

- Different geners dominate in the cities on Monday's morning and Friday's evening.

- Moscow prefers pop music, while Saint-Petersburg prefers rap.

## Проделанные шаги / Workflow
Все этапы проекта были выполнены с использованием `базового Python` и библиотеки `pandas`

All steps of this project are done with `basic Python` and `pandas` library.

### Данные / Data
На этом этапе мы прочитали данные в датафрэйм, посмотрели на первые десять строк таблицы и вывели описание данных с помощью метода `info`. В данных были найдены проблемы, которые могли оказать влияние на конечный результат исследования или затруднить работу с ними. Например, в названии колонок не было единого стиля. Также, в трех колонка были обнаружены пропуски.

Data was read into dataframe, first ten rows were checked and summary was called using `info` method. Data contained issues that might have interfere final result or make the analysis of the data harder. Namely, column names did not hold a unified style. Moreover, three columns contained missing values.

### Предобработка данных / Data preprocessing
Привели названия колонк к единому стилю, проанализировали и вставили пропуски, изучили дубликаты.


### Проверка гипотез / Hypotheses testing
Проверили 3 гипотезы оповедении пользователей двух столиц в приложении Яндекс.Музыка. Одна гипотеза подтвердилась, вторая - нет, а третья подтвердилась частично.