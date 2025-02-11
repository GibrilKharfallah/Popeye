FROM maven:3.9.6-eclipse-temurin-21-alpine AS builder

WORKDIR /app

COPY . .

RUN mvn dependency:resolve
RUN mvn package

FROM eclipse-temurin:21-jre-alpine

WORKDIR /app

COPY --from=builder /app/target/worker-jar-with-dependencies.jar .

EXPOSE 8080

CMD [ "java", "-jar", "worker-jar-with-dependencies.jar" ]

