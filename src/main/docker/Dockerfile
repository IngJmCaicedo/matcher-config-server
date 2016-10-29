FROM frolvlad/alpine-oraclejdk8:slim
VOLUME /tmp
ADD matcher-config-server-*.jar app.jar
EXPOSE 9091
RUN sh -c 'touch /app.jar'
ENTRYPOINT ["java","-Deureka.client.serviceUrl.defaultZone=http://matcher-discovery-server:9090/eureka/","-jar","/app.jar"]
