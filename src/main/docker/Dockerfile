FROM quay.io/quarkus/quarkus-distroless-image:1.0
COPY target/*-runner /application
COPY target/classes/wait-for-it.sh /wait-for-it.sh
COPY target/classes/V1.0.0__initial.sql /db/V1.0.0__initial.sql

EXPOSE 8080
USER nonroot

CMD ["./application", "-Dquarkus.http.host=0.0.0.0"]