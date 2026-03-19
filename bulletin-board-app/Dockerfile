FROM node:16-alpine
RUN apk add --no-cache curl

WORKDIR /usr/src/app
COPY package.json .
RUN npm install

EXPOSE 8080
CMD [ "node", "server.js" ]

COPY . .

HEALTHCHECK --interval=90s \
  CMD curl --fail http://localhost:8080 || exit 1  