FROM tomcat:9.0-jdk17-temurin

COPY . /app
WORKDIR /app

RUN ./mvnw package -DskipTest

RUN cp /app/target/*.war /usr/local/tomcat/webapps/ROOT.war
CMD ["cataline.sh","run"]