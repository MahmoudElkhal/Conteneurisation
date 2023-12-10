# syntax=docker/dockerfile:1
# FROM eclipse-temurin:17-jdk-jammy
FROM openjdk:22-ea-jdk-slim
WORKDIR /app
COPY .mvn/ .mvn
COPY mvnw pom.xml ./
COPY src ./src
RUN ./mvnw install -DskipTests
RUN chmod +x mvnw 
CMD ["./mvnw", "spring-boot:run"]