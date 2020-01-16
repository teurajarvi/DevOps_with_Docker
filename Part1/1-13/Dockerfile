FROM openjdk:8

EXPOSE 8080

COPY ./spring-example-project-master /usr/src/java-spring
WORKDIR /usr/src/java-spring
RUN ./mvnw package
CMD ["java", "Main"]
