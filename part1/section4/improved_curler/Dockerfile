FROM ubuntu:20.04

WORKDIR /usr/src/app

RUN apt update
RUN apt install -y curl

COPY curler.sh .

RUN chmod +x curler.sh

ENTRYPOINT ["./curler.sh"]
