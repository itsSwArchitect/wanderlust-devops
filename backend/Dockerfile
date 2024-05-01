FROM node:18.14.2

WORKDIR /app

COPY . .

RUN npm i

COPY .env.sample .env

EXPOSE 5000

CMD ["npm","start"]