FROM openjdk:8-slim
ADD gradlew gradlew
ADD build.gradle build.gradle
ADD gradle gradle
ADD settings.gradle settings.gradle
RUN ./gradlew build
RUN apt update  -y && apt install -y wget
RUN apt-get install -y procps
ADD . .
RUN ./gradlew jar
