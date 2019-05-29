FROM ubuntu:16.04
COPY . .
RUN chmod +x ./start.sh
RUN apt-get update && apt-get install curl -y
ENTRYPOINT ["./start.sh"]
