# Домашнее задание к занятию «Индексы»

### Задание 1

Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.

```SQL
SELECT table_schema, sum(index_length / data_length) * 100 "Size in %"
FROM information_schema.TABLES
GROUP BY table_schema
HAVING table_schema = "sakila";
```

