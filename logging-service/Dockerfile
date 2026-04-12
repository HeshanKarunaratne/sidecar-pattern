FROM openjdk:21

VOLUME /tmp
VOLUME /logs

WORKDIR /app

COPY ./target/log-service.jar /app

EXPOSE 8091

CMD ["java", "-jar", "log-service.jar"]