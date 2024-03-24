# Домашнее задание к занятию "`Индексы`" - `Шафиков Ринат`

### Задание 1

`Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.`

### Решение 1

Информация о таблицах базы (размеры индексов INDEX_LENGTH и размеры таблиц DATA_LENGTH)

```
select INDEX_LENGTH, DATA_LENGTH  
from information_schema.tables
where TABLE_SCHEMA = 'sakila';
```

![*](img/*.png)

---

### Задание 2

`Выполните explain analyze следующего запроса:`



```sql
select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id
```
- `перечислите узкие места;

`
- `оптимизируйте запрос: внесите корректировки по использованию операторов, при необходимости добавьте индексы.`

### Решение 2

```

```

![*](img/*.png)

---

### Задание 3

`Самостоятельно изучите, какие типы индексов используются в PostgreSQL. Перечислите те индексы, которые используются в PostgreSQL, а в MySQL — нет.
Приведите ответ в свободной форме.`

### Решение 3

```

```

![*](img/*.png)

---
