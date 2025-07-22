# ✅ Use a working Maven + Java 17 image
FROM maven:3.9.6-eclipse-temurin-17

# Set working directory
WORKDIR /app

# Copy pom.xml and source files
COPY pom.xml .
COPY src ./src

# Build the Spring Boot app
RUN mvn clean package -DskipTests

# Expose port (Render will automatically use $PORT)
EXPOSE 8080

# Run the generated jar file
CMD ["sh", "-c", "java -jar target/*.jar"]
