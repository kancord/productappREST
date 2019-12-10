# product-app-rest
## Описание
1. REST-метод, возвращающий продукт по id. Класс Product имеет поля: productId (id), productName (name), price (целочисленный тип). В случае отсутствия продукта в базе он создается при вызове метода, цена генерируется в диапазоне от 1 до 5000. Правило для формирования имени продукта: "Product" + id.
2. REST-метод для создания продукта в базе.
3. REST-метод для обновления продукта в базе. Любые имена и положительные цены.
4. REST-метод для удаления продукта.
5. Метод для возвращения всех существующих в базе продуктов.
6. Интерфейс для работы с продуктами: создание, отображение, удаление, обновление.
## Компоненты
1. Java (протестировано для 8 и 13 версий).
2. Apache Tomcat (протестировано для 8 и 9 версий).
## Запуск
1. Изменить путь базы данных на необходимый в файле main/resources/db.properties. Например: 
```
jdbc.url=jdbc:h2:C:/Projects/product-app-rest/h2db
```
2. Добавить конфигурацию Tomcat Server:
* Add new configuration -> Tomcat Server -> Local
* Указать необходимый Application Server (путь до Tomcat)
* Выбрать необходимый порт
* На закладке Deployment добавить Artifact (один из двух, например war exploded). Указать Application context: /
3. Запустить приложение. Имя пользователя/пароль для проверки: user/user
Для тестирования автоматического создания продукта использовать запрос вида:
```
http://localhost:8080/products/{id}
```
