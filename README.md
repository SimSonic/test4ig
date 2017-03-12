## Тестовое задание для [improve group](http://improve-group.ru/).
Веб-приложение, позволяющее осуществлять поиск товаров в простом прайс-листе по одному или нескольким критериям.

### Требования
* Apache Tomcat 7 / 8 / 9
* Java 8

### Установка
Скачайте целевой ```.war``` файл последней версии [со страницы задачи Jenkins](https://ci.methuselah.ru/job/test4improvegroup/).
Установите его в Tomcat, используя Manager app. Адрес для обращения к приложению должен быть вида ```<tomcat server>/test4ig/```.

### Набор тестовых данных
Исходные данные найдены в открытом доступе и предзагружены в тестовую базу данных. Адрес и учётные данные для
подключения к тестовой базе данных указаны в файле ```META-INF/persistence.xml```. Полный дамп исходных данных
также приложен в файле ```database_example_contents.sql```.