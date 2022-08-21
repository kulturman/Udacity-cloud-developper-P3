FROM node:16.13.1 as ionic

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm i -g @ionic/cli

RUN npm i --force

COPY . .

RUN ionic build

FROM nginx:alpine

#COPY www /usr/share/nginx/html
COPY --from=ionic /usr/src/app/www /usr/share/nginx/html