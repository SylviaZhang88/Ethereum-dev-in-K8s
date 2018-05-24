FROM ubuntu:14.04

COPY sources.list /etc/apt

RUN apt-get -y update && apt-get install -y wget && apt-get install -y xz-utils 

RUN wget https://npm.taobao.org/mirrors/node/v8.11.1/node-v8.11.1-linux-x64.tar.xz \ 
    && tar -xvf node-v8.11.1-linux-x64.tar.xz \
    && mv node-v8.11.1-linux-x64 /opt/ \ 
    && sudo ln -s /opt/node-v8.11.1-linux-x64/bin/node /usr/local/bin/node \ 
    && sudo ln -s /opt/node-v8.11.1-linux-x64/bin/npm /usr/local/bin/npm \
    && rm -f node-v8.11.1-linux-x64.tar.xz \
    && rm -rf node-v8.11.1-linux-x64/

RUN npm install -g bower