FROM ubuntu:14.04

ENV MONGO_MAJOR 3.6
ENV MONGO_VERSION 3.6.5

RUN sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5 \ 
    && echo "deb [ arch=amd64 ] http://mirrors.aliyun.com/mongodb/apt/ubuntu trusty/mongodb-org/$MONGO_MAJOR multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-$MONGO_MAJOR.list \ 
    && sudo apt-get -y update \
    && sudo apt-get install -y mongodb-org=$MONGO_VERSION mongodb-org-server=$MONGO_VERSION mongodb-org-shell=$MONGO_VERSION mongodb-org-mongos=$MONGO_VERSION mongodb-org-tools=$MONGO_VERSION --force-yes

RUN mkdir -p /data/db /data/configdb \
    && chown -R mongodb:mongodb /data/db /data/configdb
VOLUME /data/db /data/configdb

EXPOSE 27017
CMD ["mongod"]
