FROM ubuntu:latest

WORKDIR /mydir
COPY ./curler.sh .
RUN chmod a+x ./curler.sh
RUN apt-get update && apt-get install -y curl

CMD ["./curler.sh"]
