# spring-boot-microservices

Проект на Spring Boot для курса "Современные компьютерные технологии"

Автор: Степан Морозов, ИВТ21-МО

# Инструменты
1. Spring Boot 2.3.6
2. H2 database
3. Spring Cloud
4. Spring Data
5. JDK 11
6. Maven 3.6.3

# Проект employees-management

Реализация CRUD-операций с помощью Spring Boot.
В качестве базы данных используется Н2. Данные для БД хранятся в файле `resources/data.sql`. 

Скриншот приложения:

![alt text](https://i.imgur.com/bgCUu2f.jpeg)


# Проект currency-exchange

Сервис, возвращающий валютный коэффициаент, является `поставщиком услуг` (Service Provider). Реализован с помощью Spring Boot.
В качестве базы данных используется Н2. Данные для БД (валютные коэффициенты) хранятся в файле `resources/data.sql`. 

## API
- http://localhost:8000/currency-exchange/from/GBP/to/RUB

![alt text](https://i.imgur.com/RGfaeNg.jpeg)

# Проект currency-converter

Реализация валютного конвертера с помощью Spring Boot. Является `потребителем услуг`, обращается к `currency-exchange`, 
В качестве базы данных используется Н2. Данные для БД хранятся в файле `resources/data.sql`. 

## API
- http://localhost:8100/currency-converter/from/GBP/to/INR/quantity/500

# Проект eureka-naming-server

Приложение `eureka-naming-server` содержит информацию обо всех клиентских сервисных приложениях.
Каждый микросервис регистрируется на сервере Eureka, и Eureka знает все клиентские приложения, работающие на каждом порту и IP-адресе.
Eureka Server также известен как Discovery Server.

![alt text](https://i.imgur.com/H5JNOhP.jpeg)

# Инструкция по запуску

1. Склонировать репозиторий и его модули к себе командой `git clone --recursive`
2. Убедиться, что используется Java 11 - `java -version`, `javac -version`
3. Убедиться, что Maven установлен и узнать используемую версию Java - `mvn -version` (если версия Java отличается от версии из шага 2, то необходимо настроить переменную окружения `JAVA_HOME`)
4. Запустить `employees-management` командой `mvn spring-boot:run` из корня проекта. Приложение будет доступно по адресу localhost:8080/
5. Запустить `currency-exchange` командой `mvn spring-boot:run` из корня проекта. Приложение будет доступно по адресу localhost:8000/
6. Запустить `currency-converter` командой `mvn spring-boot:run` из корня проекта. Приложение будет доступно по адресу localhost:8100/
7. Запустить `eureka-naming-server` командой `mvn spring-boot:run` из корня проекта. Приложение будет доступно по адресу localhost:8761/
8. Приступить к работе на localhost:8080/


