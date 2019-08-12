FROM ubuntu:16.04
RUN apt-get update && apt-get install -y python python3-pip ffmpeg wget && \
    pip3 install --upgrade yle-dl && \
    rm -rf /var/lib/apt/lists 
WORKDIR /app
ENTRYPOINT [ "yle-dl" ]