# SQL-for-tinkoff

### Задание 1
```sql
Select pilots.* from pilots,flights
where pilots.id=flights.second_pilot_id
and flights.destination='Шереметьево'
GROUP BY pilots.id
HAVING COUNT(*)=3
```
Я вывел все столбы из таблицы пилотов, проверив условия для объединения таблиц и номера пилота, а также для аэропорта, а после использовал GROUP BY для возможности использования HAVING, которым проверил количество рейсов.

### Задание 2
```sql
SELECT pilots.* from pilots,planes,flights
where pilots.id=flights.first_pilot_id or pilots.id=flights.second_pilot_id
AND flights.plane_id=planes.plane_id
AND planes.cargo_flg=0
AND planes.capacity>30
```
Тут я удостоверяюсь, что пилоты и самолёты не перемешаны, учитывая и первого и второго пилота, после проверяю назначение самолёта и количество пасажиров

### Задание 3
```sql
SELECT pilots.* from pilots,planes,flights
where pilots.id=flights.first_pilot_id
AND flights.plane_id=planes.plane_id
AND planes.cargo_flg=1
ORDER BY COUNT(pylots.id) DESC
```
Этот момент нужно доделать, я не уверен, что выйдет то, что нужно
