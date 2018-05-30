FROM hollycat/nodejs:latest 

COPY ethereum-api/ /opt/ethereum-api/

RUN echo '192.168.0.150 mongodb.geth.leadingsoft.com ws.geth.leadingsoft.com' >> /etc/hosts  \
    && apt-get install -y git  \ 
    && cd /opt/ethereum-api/  \
    && bower update  --force-latest --allow-root  \
    && npm install  \
    && bower install --allow-root 

WORKDIR /opt/ethereum-api

CMD npm start