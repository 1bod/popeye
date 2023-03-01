FROM node:12-alpine

COPY package.json .
RUN npm i -y

COPY . .

CMD ["node", "server.js"]

EXPOSE 80