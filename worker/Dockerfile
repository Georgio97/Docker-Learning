FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /builder
COPY . .
RUN mvn dependency:resolve
RUN mvn package


FROM openjdk:8-jre-alpine
COPY --from=builder /builder/target .
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]