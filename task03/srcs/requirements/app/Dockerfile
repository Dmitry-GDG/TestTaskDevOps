FROM debian:buster

RUN apt-get -y update && \
    apt-get -y install git default-jdk && \
	git clone https://github.com/callicoder/spring-boot-postgresql-jpa-hibernate-rest-api-demo.git /java_app && \
	cd /java_app && \
    mvn clean package && \
	mvn compile && \
	java -jar target/postgres-demo-0.0.1-SNAPSHOT.jar

CMD supervisord
