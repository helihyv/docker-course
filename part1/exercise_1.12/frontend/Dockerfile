
FROM ubuntu:16.04
WORKDIR /mydir
EXPOSE 5000
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install -g serve
ENV API_URL=http://localhost:8000
COPY . .
RUN npm install
RUN npm run build
ENTRYPOINT /usr/bin/serve -s -l 5000 dist





