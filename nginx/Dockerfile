FROM ubuntu:20.04

RUN apt update && apt install -y nginx && \
apt clean && apt autoclean && apt autoremove

CMD [ "nginx", "-g", "daemon off;" ]