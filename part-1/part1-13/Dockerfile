FROM openjdk:8

WORKDIR /myapp
COPY ./spring-example-project /myapp

RUN ./mvnw package
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
EXPOSE 8080
