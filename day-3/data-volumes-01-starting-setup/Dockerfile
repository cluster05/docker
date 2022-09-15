FROM node

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . .

EXPOSE 80

VOLUME [ "/app/feedback" ]

CMD [ "node","server.js" ]




