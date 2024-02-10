# Домашнее задание к занятию «SQL. Часть 2»

### Задание 1

Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.

SELECT DISTINCT district FROM address WHERE district LIKE 'K%a' AND district NOT LIKE '% %';

![image](https://github.com/ZelinskiyAN/test-zabbix/assets/149052655/621b5c67-ddb7-4161-8e72-0689aaeee51a)


### Задание 2

Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.

SELECT amount, payment_date FROM payment WHERE amount > 10 AND payment_date BETWEEN '2005-06-15 00:00:00' AND '2005-06-18 23:59:59';

![image](https://github.com/ZelinskiyAN/test-zabbix/assets/149052655/0d347d20-033b-4827-a117-2f9bd6e62f64)


### Задание 3

Получите последние пять аренд фильмов.

SELECT rental_id, rental_date, last_update  FROM rental ORDER BY rental_date DESC, rental_id DESC LIMIT 5;

![image](https://github.com/ZelinskiyAN/test-zabbix/assets/149052655/a066047c-9848-4fc3-bb4a-1547f14843b9)


### Задание 4

Одним запросом получите активных покупателей, имена которых Kelly или Willie.

Сформируйте вывод в результат таким образом:

все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
замените буквы 'll' в именах на 'pp'.

SELECT LOWER(first_name), LOWER(last_name), REPLACE(LOWER(first_name), 'll', 'pp')as ll_TO_pp FROM customer WHERE first_name LIKE 'Kelly' OR  first_name  LIKE 'Willie';

![image](https://github.com/ZelinskiyAN/test-zabbix/assets/149052655/b617b828-f485-41f1-81e2-f6e874201160)
