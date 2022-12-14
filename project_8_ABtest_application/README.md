# Анализ поведения пользователей мобильного приложения

## Данные
Каждая запись в логе — это действие пользователя, или событие:
- название события;
- уникальный идентификатор пользователя;
- время события;
- номер эксперимента:
  - 246 и 247 - контрольные группы, а 248 — экспериментальная.


## Цели
 - Изучить воронку продаж.
- Выяснить, какой шрифт лучше.

## Этапы
1. Обзор и подготовка данных:
- замена названий столбцов;
- проверка на пропуски и дубликаты;
2. Проверка данных:
- изучение количества событий и количества пользователей в логе;
- оптимизация временного отрезка проведения эксперимента.
3. Воронка событий:
- сортировка событий по частоте;
- сортировка событий по числу пользователей;
- построение и анализ воронки;
- конверсия.
4. Результаты A/A/B эксперимента:
- поиск статистически значимых различий между контрольными группами;
- поиск статистически значимых различий между контрольными и экспериментальной группами.
5. Общий вывод.

## Библиотеки
- pandas
- datetime
- seaborn
- plotly
- matplotlib
- numpy
- scipy
- math

## Выводы
- в эксперименте изначально участвовало 7_551 пользователь;
- в среднем на одного пользователя приходится около 20 событий;

- Воронка продаж показала, что с главного экрана на экран с предложением переходит 61.5% пользователей, от предложения к корзине - 49.8% от изначального количества пользователей; от корзины к экрану с успешной оплатой - 47.2%. Больше всего пользователей теряется при переходе с главного экрана на экран с предложением.

**Проверка гипотез**
В ходе проверки гипотезы о равенстве долей, при уровне статистической значимости 0.05 различий между контрольными группами обнаружено не было. Статистических различий между контрольными и экспериментальной группой обнаружено также не было. Для исключения ошибки первого рода уровень значимости был снижен до 0.005. По итогам финального теста можно сделать вывод, что статистически значимых отличий между группами нет.

**Рекомендации**
По итогам исследования можно сделать вывод, что контрольные группы со старыми шрифтами и экспериментальная группа с новыми шрифтами по конверсии не отличаются. Возможно, имеет смысл изучить другие метрики.
