FROM maven:3.5-jdk-8-alpine as builder
LABEL vendor="Bastien"

WORKDIR /src
ADD . /src
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
LABEL vendor="Bastien"

WORKDIR /src
COPY --from=builder /src/target/ ./
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]