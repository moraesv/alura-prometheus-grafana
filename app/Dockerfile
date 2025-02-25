FROM openjdk:8-jdk-alpine

RUN addgroup -S spring && adduser -S spring -G spring

RUN apk add --no-cache curl

USER spring:spring

ARG JAR_FILE=target/*jar
COPY ${JAR_FILE} app.jar

ENTRYPOINT ["java","-Xms128M","-Xmx128M","-XX:MetaspaceSize=64m","-XX:MaxMetaspaceSize=128m","-Dspring.profiles.active=prod","-jar","/app.jar"]