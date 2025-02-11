FROM node:21-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN rm -rf node_modules

EXPOSE 80

CMD [ "node", "server.js" ]