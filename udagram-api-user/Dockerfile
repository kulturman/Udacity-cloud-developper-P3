FROM node:latest

WORKDIR /usr/src/app

COPY package*.json ./

RUN curl -v https://registry.npmjs.com/

RUN npm install

COPY . .

EXPOSE 8080

CMD [ "npm", "run", "prod" ]