
FROM node:alpine
WORKDIR /mydir
COPY . .
EXPOSE 5000
RUN npm install -g serve && \
    npm install && \
    npm run build && \
    adduser -D app
USER app
ENTRYPOINT /usr/local/bin/serve -s -l 5000 dist





