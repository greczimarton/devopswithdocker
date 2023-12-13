FROM node:16.20.2-buster

EXPOSE 5001

WORKDIR /usr/src/app

RUN npm install -g serve

COPY . .

RUN npm install

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm run build

CMD ["serve", "-s", "-l", "5001", "build"]
