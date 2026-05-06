FROM node:22-alpine

RUN addgroup api && adduser -S -G api api

USER api

WORKDIR /api

COPY package*.json /api/

RUN npm ci --omit=dev

COPY . .

EXPOSE 3000

CMD [ "node", "./server.js" ]