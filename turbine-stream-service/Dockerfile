FROM openjdk:8
MAINTAINER Chi Dov <d.chiproeng@gmail.com>
ADD ./target/turbine-stream-service.jar /app/
ADD ./java-agent/* /app/
CMD ["java","-javaagent:/app/nudge-3.5.0.jar","-jar","/app/turbine-stream-service.jar"]
EXPOSE 8989