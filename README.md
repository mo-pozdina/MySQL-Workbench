# MySQL-Workbench. Основы баз данных. Базовые запросы SQL. 
Здесь можно посмотреть базовые запросы __SQL__ в программе __MySQL Workbench__ для таблицы: 
![скрин](https://raw.githubusercontent.com/mo-pozdina/MySQL-Workbench/main/%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D0%91%D0%94.png)
__Список команд: CREATE, SELECT, WHERE, DROP, INSERT, UPDATE, ORDER BY, LIMIT, DELETE.__

# CREATE
```
CREATE TABLE `amperka`.`kits` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `product` VARCHAR(100) NOT NULL,
  `quantity` VARCHAR(100) NOT NULL,
  `price` INT NOT NULL,
  `сollection` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`id`))
ENGINE = InnoDB
DEFAULT CHARACTER SET = utf8
COLLATE = utf8_bin;
 ```
![скрин](Requests/CREATE.png)

```
CREATE TABLE `amperka`.`kits` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `product` VARCHAR(100) NOT NULL,
  `quantity` VARCHAR(100) NOT NULL,
  `price` INT NOT NULL,
  `сollection` VARCHAR(45) NOT NULL,
  `region` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`id`))
ENGINE = InnoDB;
 ```
![скрин](Requests/CREATE2.png)
# SELECT
```
SELECT * FROM amperka.kits;
 ```
![скрин](Requests/SELECT.png)

```
use amperka;
SELECT * FROM kits;
 ```
![скрин](Requests/SELECT2.png)

```
SELECT product, сollection FROM kits;
 ```
![скрин](Requests/SELECT3.png)
# WHERE
```
SELECT * FROM kits WHERE id=2;
 ```
![скрин](Requests/WHERE.png)

```
SELECT * FROM kits WHERE (product='CyberLight') OR (сollection='Arduino') LIMIT 2;
 ```
![скрин](Requests/WHERE_OR_LIMIT.png)

```
SELECT * FROM kits WHERE (price>6000) AND (region='Москва');
 ```
![скрин](Requests/WHERE_AND.png)
# DROP
```
DROP TABLE `amperka`.`kits`;
 ```
![скрин](Requests/DROP.png )
# INSERT
```
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('Малина v4 (2 ГБ)', 'Сейчас нет', '18490', 'Raspberry Pi', 'Санкт-Петербург');
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('Матрёшка Z', 'В наличии более 50 шт.', '6740', 'Arduino', 'Москва');
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('Планета XOD', 'В наличии всего 7 шт.', '6740', 'Arduino', 'Доставка по России');
 ```
![скрин](Requests/INSERT.png )

```
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('Трасса для Драгстера', 'В наличии всего 5 шт.', '9900', 'Школам и кружкам', 'Москва');
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('Электроника для начинающих (часть 1)', 'В наличии всего 7 шт.', '5490', 'Детям', 'Москва');
INSERT INTO `amperka`.`kits` (`product`, `quantity`, `price`, `сollection`, `region`) VALUES ('CyberLight', 'В наличии более 10 шт.', '640', 'Пайка', 'Доставка по России');
 ```
![скрин](Requests/INSERT2.png)
# UPDATE
```
UPDATE kits SET quantity ='В наличии всего 10 шт' Where id>5;
 ```
![скрин](Requests/UPDATE.png)
# ORDER BY
```
SELECT * FROM kits ORDER BY price;
 ```
![скрин](Requests/ORDER_BY.png)
# LIMIT
```
SELECT * FROM kits LIMIT 2;
 ```
![скрин](Requests/LIMIT.png)
# DELETE
```
DELETE FROM kits WHERE id>6;
 ```
![скрин](Requests/DELETE.png)
