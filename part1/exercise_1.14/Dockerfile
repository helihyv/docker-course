FROM openjdk:13
WORKDIR mydir
COPY . .
RUN ./mvnw package
ENTRYPOINT java -jar ./target/docker-example-1.1.3.jar
