# Анализ оттока клиентов фитнес-центра

## Данные
1. Данные клиента за предыдущий до проверки факта оттока месяц:
- пол;
- проживание или работа в районе, где находится фитнес-центр;
- сотрудник компании-партнёра клуба (сотрудничество с компаниями, чьи сотрудники могут получать скидки на абонемент — в таком случае фитнес-центр хранит информацию о работодателе клиента);
- факт первоначальной записи в рамках акции «приведи друга» (использовал промо-код от знакомого при оплате первого абонемента);
- наличие контактного телефона;
- возраст;
- время с момента первого обращения в фитнес-центр (в месяцах).
2. Информация на основе журнала посещений, покупок и информация о текущем статусе абонемента клиента:
- длительность текущего действующего абонемента (месяц, 6 месяцев, год);
- срок до окончания текущего действующего абонемента (в месяцах);
- факт посещения групповых занятий;
- средняя частота посещений в неделю за все время с начала действия абонемента;
- средняя частота посещений в неделю за предыдущий месяц;
- суммарная выручка от других услуг фитнес-центра: кафе, спорттовары, косметический и массажный салон.
- факт оттока в текущем месяце.

## Цель
Провести анализ и подготовить план действий по удержанию клиентов.

## Этапы
1. Загрузка данных;
2. Исследовательский анализ данных (EDA);
3. Построение модели прогнозирования оттока клиентов;
4. Кластеризация клиентов;
5. Общие выводы и рекомендации.

## Библиотеки
- pandas
- seaborn
- pyplot
- scikit-learn

## Выводы
- фитнес-центр посещает одинаковое количество мужчин и женщин, имеющие возраст в среднем 29 лет (+- 3 года), большинство проживает поблизости;
- клиенты предпочитают брать абонемент на месяц или полгода, около 41% посещают групповые занятия. В среднем клиенты посещают фитнес-центр 2 раза в неделю.

**Кластеризация**
В ходе кластеризации были выделены следующие группы клиентов: 1) Первый и второй кластены (отображены на дендрограмме фиолетовым и красным цветами соответственно): наиболее многочисленные (1003 и 971 клиент) и наименее подвержены оттоку. Это клиенты старше 29 лет, проживают поблизости от фитнес-центра, обладатели абонементов на полгода, посещающие фитнес-центр не менее 4-5 месяцев, стабильно 2 раза в неделю; большинство из них посещает групповые занятия и тратят на доп.услуги больше, чем остальные. Как правило это люди, являющиеся сотрудниками компаний-партнеров, и/или пришедшие по акции "приведи друга".
2) Третий и четвертый кластеры (оранжевый и зеленый цвета на дендрограмме): вместе составляют чуть более половины от суммы первых двух; здесь сосредоточен самый большой процент оттока. Это "младшие" клиенты (меньше 29 лет), купившие абонемент на месяц и посещающие фитнес-центр менее двух раз в неделю. Как правило если такой клиент начинает появляться в клубе один раз в неделю и реже - это означает, что вскоре он уйдет в отток. Такие клиенты реже посещают групповые занятия и меньше тратят на доп.услуги.

**Рекомендации*
Взаимодействие с клиентами имеет смысл вести в двух направлениях:
1) делать ставку на клиентов постарше (вне зависимости от пола) и платежеспособных (готовых посещать доп.занятия и тратиться в фитнес-центре на доп.услуги); продолжать и расширять сотрудничество с компаниями, как "поставщиками" самых лояльных клиентов.
2) учитывая, что в отток уходят самые молодые клиенты, можно поработать прицельно с этой аудиторией с целью ее удержания:
- организовать групповые занятия (фактор, уменьшающий отток), ориентированные именно на молодую аудиторию;
- придумать альтернативу компаниям-партнерам (например, заключать аналогичные договоры с колледжами и вузами).
