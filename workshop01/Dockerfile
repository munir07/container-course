FROM node:latest

ENV APP_PORT=3000 APP_DIR=/app DB_HOST=mydb DB_USER=root DB_PASSWORD=changeit DB_PORT=3306

WORKDIR ${APP_DIR}

ADD config config
ADD public public
ADD views views

ADD package.json .
ADD package-lock.json .

RUN npm install

ADD main.js .

EXPOSE ${APP_PORT}

ENTRYPOINT [ "node", "main.js" ]
CMD [ "{$APP_PORT}" ]
