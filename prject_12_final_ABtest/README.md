# А/В-тестирование
## Данные
- календарь маркетинговых событий на 2020 год.

*Структура файла `marketing_events`:*

- название маркетингового события;
- регионы, в которых будет проводиться рекламная кампания;
- дата начала кампании;
- дата завершения кампании.
- пользователи, зарегистрировавшиеся с 7 по 21 декабря 2020 года.

*Структура файла `users`:*

- идентификатор пользователя;
- дата регистрации;
- регион пользователя;
- устройство, с которого происходила регистрация.
- действия новых пользователей в период с 7 декабря 2020 по 4 января 2021 года.

*Структура файла `events`*:

user_id — идентификатор пользователя;
- дата и время покупки;
- тип события;
- дополнительные данные о событии. Например, для покупок, purchase, в этом поле хранится стоимость покупки в долларах.
- таблица участников тестов.

Структура файла `participants`:

- идентификатор пользователя;
- название теста;
- группа пользователя.

## Этапы
- общий обзор и первичная обработка данных;
- проверка тестовой аудитории с конкурирующим тестом на пересечения;
- проверка данные на соответствие ТЗ;
-  исследовательский анализ данных;
- построение и изучение продуктовой воронки;
- проверка статистической разницы долей;
- общие выводы.

## Библиотеки
- pandas
- datetime
- pyplot
- numpy
- plotly
- math
- scipy

## Выводы
- 14% новых зарегистрированных пользователей - из Европы;
- пользователи совершают от 4 до 9 действий, хотя встречаются выбросы в 20 и более действий;
- в обеих группах пользователи чаще всего совершают от 1 до 2 действий в день.
На этапе исследовательского анализа данных выяснилось, что данные не соответствуют целому ряду требований ТЗ. По итогам анализа можно сделать вывод, что цель увеличения конверсии на 10% на каждом из этапов продуктовой воронки достигнута не была. Напротив, группа В показала ухудшение результатов почти на всех этапах. Статистически значимые отличия при помощи z-критерия были найдены только при переходе с первого на второй этап. Опираясь на продуктовую воронку можно сделать вывод, что это отличия в сторону снижения, а не увеличения конверсии (65% в группе А против 56% в группе В). Однако результаты не могут быть признаны релевантными. Необходимо повторить тест вне маркетинговых событий, с более сбалансированными по количеству группами и большим количеством участников.

## Статус
Завершен.
