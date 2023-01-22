# Музыка больших городов / Music of Big Cities

## Цель проекта / Project goal
Изучить и сравнить поведение людей из Москвы и Санкт-Петербурга в приложении Яндекс.Музыка для проверки следующих гипотез / To study and to compare the activity of people from Moscow and Saint-Peterburg in Yandex.Music app to check the following hypotheses:
- Активность пользователей двух городов отличается в зависимости от дня недели / Activity of users differs between cities depending on the day of the week.
- Утром в понедельник и в пятницу вечером в городах преобладают разные музыкальные жанры / Different geners dominate in the cities on Monday's morning and Friday's evening.
- В Москве популярен поп, а в Санкт-Петербурге - рэп / Moscow prefers pop music, while Saint-Petersburg prefers rap.

## Проделанные шаги
Все этапы проекта были выполнены с использованием `базового Python` и библиотеки `pandas` / All steps of this project are done with `basic Python` and `pandas` library.

### Знакомство и описание данных / The first look at the data and its description
На этом этапе мы прочитали данные в датафрэйм, посмотрели на первые десять строк таблицы и вывели описание данных с помощью метода `info`. В данных были найдены проблемы, которые могли оказать влияние на конечный результат исследования или затруднить работу с ними. Например, в названии колонок не было единого стиля. Также, в трех колонка были обнаружены пропуски. / Data was read into dataframe, first ten rows were checked and summary was called using `info` method. Data contained issues that might have interfere final result or make the analysis of the data harder. Namely, column names did not hold a unified style. Moreover, three columns contained missing values.

### Предобработка данных / Data preprocessing
