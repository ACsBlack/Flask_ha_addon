ARG BUILD_FROM=ghcr.io/home-assistant/aarch64-base:latest
FROM $BUILD_FROM

ENV LANG C.UTF-8

RUN apk add --no-cache python3 py3-pip \
    && pip install --no-cache-dir flask flask-sqlalchemy pymysql

WORKDIR /app
COPY . /app/

RUN chmod a+x /app/run.sh
CMD [ "/app/run.sh" ]