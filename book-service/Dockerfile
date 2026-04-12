FROM openjdk:21-ea-jdk-slim

VOLUME /tmp
VOLUME /logs

WORKDIR /app

COPY ./target/book-service.jar /app

EXPOSE 8090

CMD ["java", "-jar", "book-service.jar"]