## 3.Java приложение 

Клонировать репозиторий в локальный Bitbucket https://github.com/callicoder/spring-boot-postgresql-jpa-hibernate-rest-api-demo.git

Настроить сборку java приложения в Jenkins из локального Bitbucket (собранный образ поместить в nexus)

Создать job деплоя приложения в Jenkins (используя ранее собранный образ):

- Nginx – реверс-прокси к java приложению

- Java 

- PostgreSQL

Проверить работу приложения с помощью curl/postman