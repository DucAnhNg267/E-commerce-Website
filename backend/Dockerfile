FROM eclipse-temurin:17-jdk-jammy AS build
WORKDIR /workspace
COPY pom.xml mvnw .
COPY .mvn .mvn
RUN mvn -B -f pom.xml -q dependency:go-offline
COPY src src
RUN mvn -B -f pom.xml -q package -DskipTests

FROM eclipse-temurin:17-jre-jammy
WORKDIR /app
COPY --from=build /workspace/target/backend-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/app/app.jar"]
