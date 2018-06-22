FROM ubuntu:16.04

RUN \
  apt-get update && \
  apt-get install -y default-jdk && \
  rm -rf /var/lib/apt/lists/* \
  vim

WORKDIR /data

# Define commonly used JAVA_HOME variable
# ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

CMD ["bash"]
