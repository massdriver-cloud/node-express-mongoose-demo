FROM node:18

WORKDIR /app
COPY package.json yarn.lock .
RUN yarn install

COPY . /app
COPY ./docker/wait-for-it.sh /usr/local
RUN chmod +x /usr/local/wait-for-it.sh

EXPOSE 3000

CMD ["npm", "start"]

