FROM ubuntu:14.04

COPY sources.list /etc/apt

RUN apt-get -y update && apt-get install -y wget xz-utils g++ \ 
    && wget https://npm.taobao.org/mirrors/node/v8.11.1/node-v8.11.1-linux-x64.tar.xz \ 
    && tar -xvf node-v8.11.1-linux-x64.tar.xz \
    && mv node-v8.11.1-linux-x64 /opt/ \ 
    && sudo ln -s /opt/node-v8.11.1-linux-x64/bin/node /usr/local/bin/node \ 
    && sudo ln -s /opt/node-v8.11.1-linux-x64/bin/npm /usr/local/bin/npm \
    && sudo apt-get install -y software-properties-common python-software-properties  \
    && sudo add-apt-repository -y  ppa:ubuntu-toolchain-r/test  \
    && sudo apt-get -y update \
    && sudo apt-get -y upgrade  \
    && sudo apt-get -y dist-upgrade  \
    && rm -f node-v8.11.1-linux-x64.tar.xz \
    && rm -rf node-v8.11.1-linux-x64/

RUN npm install -g bower  \
    && ln -s /opt/node-v8.11.1-linux-x64/bin/bower /usr/local/bin/bower

CMD ["node -v"]