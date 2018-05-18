FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD spring2.jar /opt/spring2/
EXPOSE 8080
WORKDIR /opt/spring2/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "spring2.jar"]
