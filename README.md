# Мини-проект
ПОСТАНОВКА ЗАДАЧИ

Результаты A/A/B-тестирования от одного известного маркетплейса:

sample_a, sample_c — АА-группы, sample_b — отдельная группа.

В каждом датасете есть три типа действий пользователей:

0 — клик,
1 — просмотр
2 — покупка пользователь просматривает выдачу товаров, кликает на понравившийся товар и совершает покупку.
Маркетплейс ориентируется на следующие метрики:

ctr (отношение кликов к просмотрам товаров);
purchase rate (отношение покупок к просмотрам товаров);
gmv (оборот, сумма произведений количества покупок на стоимость покупки), где считаем 1 сессию за 1 точку (1 сессия на 1 пользователя).
Данные уже почищены по сессиям, вы можете использовать их в агрегированном виде. Ваша задача — понять, нет ли проблемы с разъезжанием сплитов и улучшает ли алгоритм B работу маркетплейса.

Тест Шапиро-Уилка проведите на alpha=0.01

Что важно как требование к чистоте данных?
Посмотрите внимательно на значения метрик!
«Разъезжаются» ли сплиты? Посмотрите на результаты A/A-теста.
Каков результат А/B-теста? можем ли мы на него положиться?
ПЛАН ПРОЕКТА

Предварительная обработка датасета
(Проверка, что нет ситуаций, когда происходит покупка/клик без действия просмотра. Удаление дублей.)

Рассчет метрик по датасетам, общее сравнение метрик.

Тест равенства долей для A и C групп по всем метрикам.

Тест равенства долей для A и B групп по всем метрикам.
