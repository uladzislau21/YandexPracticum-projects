# Защита персональных данных клиентов / Protection of clients' personal data

## Цель проекта / Project goal
Изучить линейную алгебру и применить её для построения алгоритма шифрования персональных данных клиентов страховой компании. Убедиться, что преобразованные данные не понижают качество моедли машинного обучения.

To study linear algebra and apply it to build an algorithm for encrypting personal data of insurance company clients. Ensure that the transformed data does not decrease the quality of the machine learning model.

## Проделанные шаги / Workflow

### Данные / Data
В качестве данных использовали персональную информацию о клиентах страховой компании: пол, возраст, зарплата, количество членов семьи, страховые выплаты.

Personal information about the clients of the insurance company was used: gender, age, salary, number of family members, insurance payments.

### Изучение умножения матриц / Matrices multiplication studying
На данном этапе изучили как происходит умножение матриц, что такое единичная матрица, изучили алгоритм линейной регрессии в матричном виде. Математически доказали, что преобразование не меняет исходные данные.

At this stage, we studied how matrix multiplication occurs, what an identity matrix is, we studied the linear regression algorithm in matrix form. Mathematically proved that the transformation does not change the original data.

### Проверка алгоритма преобразования / Transformation algorithm check
Обучили модель линейной регрессии на оригинальных и преобразованных данных, сравнили метрики.
