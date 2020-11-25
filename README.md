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

# Инструкция по запуску

1. Склонировать репозиторий и его модули к себе командой `git clone --recursive`
2. Убедиться, что используется Java 11 - `java -version`, `javac -version`
3. Убедиться, что Maven установлен и узнать используемую версию Java - `mvn -version` (если версия Java отличается от шагов 2 и 3, то необходимо настроить JAVA_HOME)
4. Запустить `employees-management` командой `mvn spring-boot:run` из корня проекта. Приложение запуститься на localhost:8080/
5. Запустить `currency-exchange` командой `mvn spring-boot:run` из корня проекта. Приложение запуститься на localhost:8000/
6. Запустить `currency-converter` командой `mvn spring-boot:run` из корня проекта. Приложение запуститься на localhost:8100/
7. Запустить `eureka-naming-server` командой `mvn spring-boot:run` из корня проекта. Приложение запуститься на localhost:8761/
8. Приступить к работе на на localhost:8080/


