FROM quay.io/thoth-station/s2i-thoth-ubi8-py36:latest

USER 0
# Needed to enable manylinux2010.
RUN pip3 install --upgrade pip
USER 1001
RUN curl https://raw.githubusercontent.com/fridex/playground/master/tensorflow-matmul/Pipfile.lock -o Pipfile.lock && \
    curl https://raw.githubusercontent.com/thoth-station/micropipenv/master/micropipenv.py | python3 - install && \
    curl https://raw.githubusercontent.com/thoth-station/performance/master/tensorflow/matmul.py -o app.py

CMD ["python3", "/opt/app-root/src/app.py"]
