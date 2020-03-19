FROM zenika/alpine-maven AS builder
RUN mkdir -p /src
WORKDIR /src
COPY pom.xml ./
RUN mvn dependency:go-offline
COPY . ./
RUN mvn package -Dmaven.test.skip=true
FROM azul/zulu-openjdk-alpine:11-jre
COPY target/demo*.jar /app.jar
CMD ["java", "-jar", "/app.jar"]

