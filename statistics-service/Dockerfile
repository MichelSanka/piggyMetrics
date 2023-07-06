FROM openjdk:8
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>
ADD ./target/statistics-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/statistics-service.jar"]
EXPOSE 7000