FROM node:21 AS backend-main-image

WORKDIR /app

COPY . .

RUN npm install

FROM node:21-slim 

COPY --from=backend-main-image /app .

COPY .env.sample .env 

EXPOSE 5000

CMD ["npm", "start"]
