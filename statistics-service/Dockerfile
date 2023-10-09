FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/statistics-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/statistics-service.jar"]
EXPOSE 7000