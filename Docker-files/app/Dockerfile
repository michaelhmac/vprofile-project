# Multistage Dockerfile

FROM openjdk:8 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/michaelhmac/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

FROM tomcat:8-jre11

RUN rm -rf /local/local/tomcat/webapp/*

COPY --from=BUILD_IMAGE vprofile-project/target/vprofile.v2.war /usr/local/tomcat/webapp/ROOT.war

EXPOSE 80:80 

CMD ["catalina.sh", "run"]
