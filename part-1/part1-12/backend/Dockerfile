FROM ubuntu

WORKDIR /myapp

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

COPY ./backend-example-docker /myapp
RUN npm install

ENV FRONT_URL=http://localhost:5050

CMD npm start
EXPOSE 8000
