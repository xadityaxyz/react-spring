# Use Maven image to build the project
FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app
COPY springboot-backend /app
RUN mvn clean package -DskipTests

# Use JDK image to run the application
FROM openjdk:17-jdk-slim
WORKDIR /app
COPY --from=build /app/target/*.jar app.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "app.jar"]
