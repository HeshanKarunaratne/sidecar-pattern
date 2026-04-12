FROM openjdk:21

VOLUME /tmp
VOLUME /logs

WORKDIR /app

COPY ./target/book-service.jar /app

EXPOSE 8090

CMD ["java", "-jar", "book-service.jar"]