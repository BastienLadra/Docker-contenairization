FROM nodebb/docker
LABEL vendor="Bastien"

ADD . /usr
WORKDIR /usr
ADD . /src
WORKDIR /src
ADD . /app
COPY ./package.json .
COPY ./server.js .
COPY ./views .1

RUN npm install -g npm
RUN npm install

EXPOSE 80

CMD ["npm", "start"]
