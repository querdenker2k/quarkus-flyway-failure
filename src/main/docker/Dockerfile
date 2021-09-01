#FROM quay.io/quarkus/quarkus-distroless-image:1.0
FROM debian:latest

COPY target/*-runner /application
COPY target/classes/wait-for-it.sh /wait-for-it.sh
COPY target/classes/postgresql /db/postgresql
COPY target/classes/config /config

EXPOSE 8080

CMD ["./application", "-Dquarkus.http.host=0.0.0.0"]