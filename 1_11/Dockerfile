
FROM maven:3-eclipse-temurin-8

WORKDIR /app

COPY . .

RUN mvn -B package

EXPOSE 8080

CMD ["java", "-jar", "target/docker-example-1.1.3.jar"]
