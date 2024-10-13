# Stage 1: Build the project using Gradle and Java 21
FROM eclipse-temurin:17-jre-jammy AS build

# Set the working directory inside the container
WORKDIR /app

# Copy the built JAR file from the previous stage
COPY ./Gateway-0.0.1.jar /app/app.jar

# Expose the application port (typically 8080 for Spring Boot)
EXPOSE 8080

# Command to run the Spring Boot application
ENTRYPOINT ["java", "-Dspring.profiles.active=docker", "-jar", "/app/app.jar"]
