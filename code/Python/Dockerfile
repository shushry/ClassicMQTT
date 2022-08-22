FROM python:3.7.6-slim-stretch

COPY qemu-arm-static /usr/bin/qemu-arm-static
RUN pip install --no-cache-dir pymodbus paho-mqtt

ADD classic_mqtt.py /
ADD support/*.py support/
CMD touch /broker-ca.pem

ENTRYPOINT ["python3", "classic_mqtt.py"]
