FROM node:10

WORKDIR /node-app

COPY . .

RUN npm install

EXPOSE 80

CMD [ "node", "server.js" ]