FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/turbine-stream-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/turbine-stream-service.jar"]
EXPOSE 8989