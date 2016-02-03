issues with permissions?
do this
mysql -u root -p

then press enter for password



enter mysql console
```
mysql
```

```
show databases;
```

```
show tables;
```

how to rename a primary key
```
ALTER TABLE animalz CHANGE column animal_id id int NOT NULL AUTO_INCREMENT;
```

how to rename a foreign key
```
ALTER TABLE animalz CHANGE column careTaker_id caretaker_id int NOT NULL;
```

how to rename a table
```
RENAME TABLE tb1 TO tb2;
```

SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name=table2.column_name;


mysql> select * from animals limit 2;
ERROR 1317 (70100): Query execution was interrupted

just redo the query. It'll work the next time.





SELECT animals.name as animal_name, caretakers.name as caretaker_name, caretakers.city as caretaker_city
FROM animals
LEFT JOIN caretakers
ON animals.caretaker_id=caretakers.id
limit 3;


SELECT COUNT(*) name FROM animals RIGHT JOIN caretakers ON animals.caretaker_id = caretakers.id WHERE caretakers.city = 'ny';


exporting a mysql database to a sql file:
- make sure you're not in the mysql console

C:/xampp/mysql/bin/mysqldump -u root -p myTestDB > C:/zooDB.sql

mysqldump -u root -p myTestDB > /Users/pavankatepalli/Desktop/zooDB.sql
for password just press enter - don't enter your computer password.
