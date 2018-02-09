FROM python:2.7.14-alpine3.6

WORKDIR /usr/src/app

RUN mkdir ./ca_certs

RUN mkdir ./certs

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY RFID_mqtt_client.py ./

COPY ./ca_certs/ca_cert.pem ./ca_certs/

COPY ./certs/python_rfid.pem ./certs/

COPY ./certs/python_rfid_key.pem ./certs/

CMD [ "python", "-u", "./RFID_mqtt_client.py"]
