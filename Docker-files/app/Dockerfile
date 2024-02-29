FROM openjdk:11 AS ARTIFACTS
WORKDIR /app
RUN apt update && apt install maven -y
RUN git clone https://github.com/bhargavavhp/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

FROM tomcat:jre11
LABEL "Project"="vprofile"
LABEL "Application"="Web_server"
LABEL "Maintainer"="bhargavavhp"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=ARTIFACTS /app/vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
