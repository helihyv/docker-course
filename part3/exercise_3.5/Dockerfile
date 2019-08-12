
FROM node:alpine as build-stage
WORKDIR /mydir
COPY . .
EXPOSE 5000
RUN npm install && \
    npm run build
FROM node:alpine
WORKDIR /app
COPY --from=build-stage /mydir/dist /app/dist
RUN  npm install -g serve && \
    adduser -D app
USER app
ENTRYPOINT /usr/local/bin/serve -s -l 5000 dist





