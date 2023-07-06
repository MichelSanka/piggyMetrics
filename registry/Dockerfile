FROM openjdk:8
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>
ADD ./target/registry.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/registry.jar"]
EXPOSE 8761