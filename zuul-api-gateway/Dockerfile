#FROM maven as build
#WORKDIR /app
#COPY . .
#RUN mvn install

FROM openjdk:11.0.10-jre
WORKDIR /app
COPY ./target/zuul-0.0.1-SNAPSHOT.jar /app 
#EXPOSE 8080
EXPOSE 9999
RUN apt-get update -y
RUN apt-get install systemd-services -y
RUN hostnamectl set-hostname api
CMD ["java", "-jar", "zuul-0.0.1-SNAPSHOT.jar"] 
