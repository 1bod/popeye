FROM maven:3.8.4-jdk-11-slim as builder

COPY . .
RUN mvn dependency:resolve \
    && mvn package


FROM openjdk:11-jre-slim

COPY --from=builder /target/ ./target/
CMD [ "java", "-jar", "target/worker-jar-with-dependencies.jar" ]