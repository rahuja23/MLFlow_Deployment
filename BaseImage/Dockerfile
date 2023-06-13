From ubuntu:20.04

RUN  apt-get update  && apt install python3-pip libpq-dev -y

WORKDIR /home
COPY . .

RUN pip3 install -r requirements.txt
ENV MLFLOW_SERVER_PORT 5000
EXPOSE $MLFLOW_SERVER_PORT
ENTRYPOINT ["sh", "/home/setup_mlflow.sh"]
