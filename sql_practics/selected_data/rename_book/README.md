## Магазин счёл, что классика уже не пользуется популярностью, поэтому необходимо создать запрос на ВЫБОРКУ данных, в котором:

* Сменить всех авторов на "Донцова Дарья".
* К названию каждой книги в начале дописать "Евлампия Романова и " ( пробел в конце).
* Цену поднять на 42% (округлить её до двух знаков после запятой). 
* Отсортировать по убыванию цены.
* Столбцы назвать author, title, price.

## Структура таблицы

<img align="center" alt="sumit" src="https://github.com/kolesnikovvitaliy/SQL_PRACTICS/blob/main/sql_practics/selected_data/rename_book/img/cx_5_1.jpg">

## Ответ базы данных должен выглядеть так:

<img align="center" alt="sumit" src="https://github.com/kolesnikovvitaliy/SQL_PRACTICS/blob/main/sql_practics/selected_data/rename_book/img/res.png">

## РЕШЕНИЕ ЗАДАЧИ:

```SQL
SELECT "Донцова Дарья" AS author,
CONCAT('Евлампия Романова и ', title) AS title, 
ROUND((price * 1.42), 2) as price

FROM book
ORDER BY price DESC;
 ```
