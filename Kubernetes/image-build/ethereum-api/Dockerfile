FROM hollycat/nodejs:latest 

COPY ethereum-api/ /opt/ethereum-api/

RUN apt-get install -y git  \ 
    && cd /opt/ethereum-api/  \
    && bower update  --force-latest --allow-root  \
    && npm install  \
    && bower install --allow-root 

WORKDIR /opt/ethereum-api

CMD npm start
