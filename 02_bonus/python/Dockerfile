FROM ubuntu:16.04

RUN \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv vim && \
  rm -rf /var/lib/apt/lists/*

WORKDIR /data

RUN echo "print 'PYTHON IS WORKING'" > test.py && python test.py

# CMD ["bash"]
