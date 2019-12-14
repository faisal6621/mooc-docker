FROM ubuntu

WORKDIR /myapp

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

COPY ./frontend-example-docker /myapp
RUN npm install

ENV API_URL=http://localhost:8090

CMD npm start
EXPOSE 5000
