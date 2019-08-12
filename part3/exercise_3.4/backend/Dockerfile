FROM node:alpine
WORKDIR /mydir    
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000
COPY . .
RUN npm install && \
    adduser -D app && \
    chown app /mydir -R
USER app    
ENTRYPOINT npm start