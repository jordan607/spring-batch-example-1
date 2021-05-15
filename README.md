# Spring Boot with Spring Batch Example 1
## Load CSV to DB
- `http://localhost:8081/load` - Trigger point for Spring Batch
- `http://localhost:8081/h2-console` - H2 Console for querying the in-memory tables.

## H2 Config
- `testdb` - Database.
- `sa` - User
- `password` - Password.

## use below config in application.properties file:
server.port=8081
spring.h2.console.enabled=true
spring.datasource.platform=h2
spring.datasource.url=jdbc:h2:mem:testdb
inputfile=classpath:users.csv

## This dosent work after spring 2.2
sprint.batch.job.enabled=false
