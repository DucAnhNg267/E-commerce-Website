Backend scaffold (Spring Boot)

Build & run locally with Maven:

```bash
mvn -f backend/pom.xml clean package
java -jar backend/target/backend-0.0.1-SNAPSHOT.jar
```

Set environment variables for `DATABASE_URL`, `DATABASE_USER`, `DATABASE_PASSWORD`, and `JWT_SECRET` before running.
