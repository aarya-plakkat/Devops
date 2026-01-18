FROM ubuntu:latest

WORKDIR /app

COPY package*.json /

RUN npm install

COPY . .

Expose 3001

CMD [ "npm", "start" ]

