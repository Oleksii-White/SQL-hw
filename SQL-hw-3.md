--  Создайте таблицу goods id title quantity;

CREATE TABLE goods (
	id integer,
	title varchar(32),
	quantity integer
); 



-- Добавьте несколько строк

INSERT INTO goods (id, title, quantity) VALUES
(1, 'apple', 1000),
(2, 'pineapple', 500),
(3, 'banana', 2000)
;



-- Добавьте поле price (integer) со значением по умолчанию 0

ALTER TABLE goods
ADD price integer;



-- Проверьте содержимое таблицы

SELECT * 
FROM goods;



-- Измените тип на numeric(8, 2)

ALTER TABLE goods
CHANGE price price numeric(8, 2);



-- Измените тип обратно на integer

ALTER TABLE goods
CHANGE price price integer;



-- Переименуйте поле на item_price

ALTER TABLE goods
CHANGE price item_price numeric(8, 2);



-- Удалите это поле

ALTER TABLE goods
DROP COLUMN item_price;
