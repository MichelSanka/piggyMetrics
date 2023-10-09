FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/registry.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/registry.jar"]
EXPOSE 8761