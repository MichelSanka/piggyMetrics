FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/account-service.jar /app/
ADD ../java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/account-service.jar"]
EXPOSE 6000