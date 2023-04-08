# Определение токсичных комментариев / Toxic comments detection

## Цель проекта / Project goal
Построить модель машинного обучения для классификации комментариев на токсичные и нетоксичные. F1-score должен быть не ниже 0.75.

Build a machine learning model to classify comments to toxic and non-toxic. F1-score must be at least 0.75.

## Проделанные шаги / Workflow

### Данные / Data
Данные содержат колонку с комментариями и колонку с бинарной переменной (токсичный и нетоксичный комментарий).

The data contains a column with comments and a column with a binary variable (toxic and non-toxic comments).

### Предобработка данных / Data preprocessing
Комментарии были очищены от стоп-слов, ссылок, html-тегов. Сленговые сокращения были приведены в полную форму, смайлы и эмотиконы были переведены в текстовый формат. Комментарии были лемматизированы и токенезированы.

Comments had been cleared of stop words, links, html tags. Slang abbreviations had been given their full form, smileys and emoticons have been translated into text format. Comments had been lemmatized and tokenized.

### Исследовательский анализ данных / Exploatory data analysis
Исследовали топ100 самых распространенных слов, затем в разбивке на токсичные и нетоксичные комментарии проверили какие самые распространенные 25 слов.

We examined the top 100 most common words, then, grouped into toxic and non-toxic comments, checked which were the most common 25 words.

### Построение модели / Model training
Построили 2 модели логистической регрессии. Одну обучили на признаках TF-IDF, а вторую - на эмбедингах **BERT**. Обе модели проверили на валидационной выборке. Модель, обученная на эмбедингах оказалась лучше и мы использовали её для проверки на тестовой выборке. F1-score на тестовой выборке составил 0.85.

We built 2 logistic regression models. One was trained on TF-IDF features, and the other was trained on **BERT** embeddings. Both models were tested on a validation set. The model trained on embeddings turned out to be better and we used it to test it on a test set. F1-score on the test sample was 0.85.