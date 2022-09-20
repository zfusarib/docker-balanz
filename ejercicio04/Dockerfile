FROM fabric8/java-alpine-openjdk8-jdk

COPY ${JAR_FILE} ./app

EXPOSE 8080

CMD ["java","-jar","/app/passwordapi.jar"]