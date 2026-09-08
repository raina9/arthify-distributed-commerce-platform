# Arthify User Service

Focused Arthify backend engineering laboratory for production-grade pagination and interview preparation.

## Database
Windows MySQL80 only:
- localhost:3306
- usersdb
- arthifyusers
- arthifyaddresses

Docker is intentionally out of scope.

## Dependencies
Spring Web, Spring Data JPA, MySQL Driver, Validation, Actuator, DevTools, Spring Boot Test.

Security, Kafka, Redis and Spring Cloud are intentionally excluded until their relevant Arthify features are implemented.

## Run
PowerShell:
```powershell
$env:DB_PASSWORD="your_mysql_password"
.\mvnw.cmd spring-boot:run
```

## Database policy
`ddl-auto: validate` — the application validates the existing schema and must not mutate it automatically.

## Learning sequence
1. DB connectivity
2. Entity mapping
3. Repository
4. Basic GET
5. Pageable/Page
6. Sorting and stable ordering
7. Limit/Offset
8. Cursor/Keyset
9. Testing
10. Query-plan and performance analysis
11. Production API hardening

## Interview rule
After every feature, explicitly record only the interview questions genuinely reinforced by that implementation across Spring Boot, Kafka, Microservices, JPA, Redis, Testing and Coding.

# Build, Run & Debug
## Build
mvn clean install

## Run
mvn spring-boot:run -Dspring-boot.run.arguments="--server.port=8081"

## Debug
mvn spring-boot:run -Dspring-boot.run.arguments="--server.port=8081" "-Dspring-boot.run.jvmArguments=-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005"

## Ports
Application: 8081
Debug: 5005