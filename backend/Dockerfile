FROM node:18-alpine AS build

WORKDIR /app

RUN apk add --no-cache python3 make g++ bash

COPY package*.json ./
RUN npm ci --omit=dev

COPY . .

EXPOSE 5007

ENV NODE_ENV=production

CMD ["npm", "start"]
