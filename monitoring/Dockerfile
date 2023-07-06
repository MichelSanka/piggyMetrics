FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/monitoring.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/monitoring.jar"]
EXPOSE 8181