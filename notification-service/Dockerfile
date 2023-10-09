FROM openjdk:8
MAINTAINER msanka@technologies.com
ADD ./target/notification-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/notification-service.jar"]
EXPOSE 8000