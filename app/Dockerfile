FROM alpine:latest

RUN apk add --no-cache python3 && \
    apk add --no-cache py3-pip

WORKDIR /app

COPY ./src /app

RUN pip3 --no-cache-dir install -r requirements.txt 
RUN export FLASK_APP=server
RUN export FLASK_RUN_PORT=8000                                                                             

# EXPOSE 8000


# ENTRYPOINT  ["python3"]

CMD ["flask run"]




















# FROM python:3-alpine3.10

# # RUN apt update && \
# # apt install -y python3 && \
# # apt install -y python3-pip && \
# # # pip3 install -r requirements.txt \
# # # export FLASK_APP=server \ 
# # mkdir /app && \
# # apt clean && apt autoclean && apt autoremove

# WORKDIR /app

# RUN pip install -r requirements.txt

# EXPOSE 8000

# # ENTRYPOINT [ "python" ]

# CMD [ "python", "server.py" ]