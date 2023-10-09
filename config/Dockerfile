FROM openjdk:8
MAINTAINER msanka@atakama-technologies.com
ADD ./target/config.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-4.0.3.jar","-jar","/app/config.jar"]
HEALTHCHECK --interval=30s --timeout=30s CMD curl -f http://localhost:8888/actuator/health || exit 1
EXPOSE 8888