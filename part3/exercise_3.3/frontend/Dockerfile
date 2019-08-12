
FROM ubuntu:16.04
WORKDIR /mydir
COPY . .
EXPOSE 5000
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install -g serve && \
    npm install && \
    npm run build && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists && \
    useradd -m app
USER app
ENTRYPOINT /usr/bin/serve -s -l 5000 dist





