## Тестовое задание для [improve group](http://improve-group.ru/).
Веб-приложение, позволяющее осуществлять поиск товаров в простом прайс-листе по одному или нескольким критериям.

### Требования
* Apache Tomcat 9 (```✓```), 8 (```✓```), 7 (не тестировался)
* Java 8

### Набор тестовых данных
Исходные данные найдены в открытом доступе и предзагружены в тестовую базу данных. Адрес и учётные данные для
подключения к тестовой базе данных указаны в файле ```META-INF/persistence.xml```. Полный дамп исходных данных
также приложен в файле ```database_example_contents.sql```.

### Known issues
* Реализация регистро-независимого поиска по колонкам ```Категория``` и ```Наименование``` основана на свойстве используемой
кодировки таблиц (```utf8_general_ci```). Этот факт может работать как-то иначе с СУБД, радикально отличающимися от MySQL.
* Для того, чтобы найти все наименования во всех категориях, введите символ ```%``` в поле ```Категория``` и/или в
поле ```Наименование```, не указывая ценовой диапазон. Это работает, потому что символ ```%``` является символом подстановки
подстроки в выражении LIKE. По этой же причине поискаовые запросы, содержащие ```%```, могут выдавать больше результатов,
чем Вы ожидаете.
