FROM node:alpine
WORKDIR app
COPY . .
RUN npm install && \
    adduser -D app
USER app
ENTRYPOINT npm start
