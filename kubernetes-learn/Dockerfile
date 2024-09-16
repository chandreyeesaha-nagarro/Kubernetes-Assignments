FROM maven:3.8.4-openjdk-17 AS build
COPY src app/src 
COPY pom.xml /app
WORKDIR /app
RUN mvn clean package -DskipTests

FROM openjdk:17-jdk-slim
COPY --from=build /app/target/kubernetes-learn-0.0.1-SNAPSHOT.jar /app/kubernetes-learn.jar
ENTRYPOINT ["java", "-jar", "/app/kubernetes-learn.jar"]