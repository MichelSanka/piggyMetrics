FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/gateway.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/gateway.jar"]
EXPOSE 4000