FROM debian

RUN apt-get update && apt-get install -y --no-install-recommends \
    python3 python3-pip
RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip3 install requests flask
COPY . /front
WORKDIR /front
CMD ["python3", "api.py"]
