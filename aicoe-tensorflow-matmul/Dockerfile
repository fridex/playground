FROM quay.io/thoth-station/s2i-thoth-ubi8-py36:latest

USER 0
# Needed to enable manylinux2010.
RUN pip3 install --upgrade pip
USER 1001
RUN curl https://raw.githubusercontent.com/fridex/playground/master/aicoe-tensorflow-matmul/Pipfile.lock -o Pipfile.lock && \
    curl https://raw.githubusercontent.com/thoth-station/micropipenv/ba98cd8e44f5bd376c28763e7a8950c8ca1da889/micropipenv.py | python3 - install && \
    curl https://raw.githubusercontent.com/thoth-station/performance/master/tensorflow/matmul.py -o app.py

CMD ["python3", "/opt/app-root/src/app.py"]
