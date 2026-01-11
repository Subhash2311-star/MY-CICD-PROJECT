# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM eclipse-temurin:17-jre-alpine

WORKDIR /opt/app

RUN mvn clean package

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar



COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]
