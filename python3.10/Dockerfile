FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive
ENV PYTHONPATH = /opt/code/

RUN echo "Asia/Shanghai" > /etc/timezone \
  && apt-get update \
  && apt-get install -y python3 curl tzdata \
  && apt-get -y autoremove --purge \
  && apt-get -y clean && apt-get -y autoclean \
  && dpkg-reconfigure -f noninteractive tzdata \
  && curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py \
  && python3 get-pip.py \
  && rm -rf /var/lib/apt/lists/* \
  && rm -rf /root/.cache && rm -rf /tmp/*

# CMD ["python3", "-m", "http.server"]
