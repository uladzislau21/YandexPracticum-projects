# Определение преспективного тарифа для телеком-компании / Determination of a prospective tariff for a telecom company

## Цель проекта / Project goal
Статистическими тестами определить наиболее выгодный тариф у телеком-компании.

Perform statistical testing to determine profitable tariff.

## Проделанные шаги / Workflow

### Данные / Data
Данные представляют собой количество звонков, смс, и интернет-трафика, которые пользователи использовали за определенный период. Также имеется датасет с ценами на услуги по каждому тарифу.

The data is the number of calls, sms, and internet traffic that users used in a given period. There is also a dataset with prices for services for each tariff.

### Полготовка данных / Data preprocessing
Изменили типы переменных. Рассчитали помесячные показатели активности на клиента. Проверили и заполнили пропуски. Рассчитали помесячную выручку на клиента.

Changed types of variables. We calculated monthly activity indicators per client. Checked and filled in the gaps. Calculate monthly revenue per client.

### Изучение данных / EDA
Рассчитали описательную статистику в разбивке по тарифам. Построили гистограммы распределения по смс, звонкам, и использованию интернета.

We calculated descriptive statistics grouped by tariffs. We built histograms of distribution by SMS, calls, and Internet use.

### Проверка гипотез / Hypotheses testing
Статистическими тестами проверили гипотезы о различии средней выручки двух тарифов, а также о различии выручки у пользователе из Москвы и других регионов.

Statistical tests were used to check hypotheses about the difference in the average revenue of the two tariffs, as well as the difference in revenue for a user from Moscow and other regions.