FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/auth-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/auth-service.jar"]
EXPOSE 5000