
FROM ubuntu:16.04
WORKDIR /mydir
EXPOSE 8000
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
COPY . .
RUN npm install
ENTRYPOINT npm start