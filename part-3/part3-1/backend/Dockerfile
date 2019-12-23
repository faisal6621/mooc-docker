FROM ubuntu

WORKDIR /myapp

COPY ./backend-example-docker /myapp

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    apt-get purge -y --auto-remove curl && \ 
    rm -rf /var/lib/apt/lists/*

CMD npm start
EXPOSE 8000
