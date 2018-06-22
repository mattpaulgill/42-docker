FROM ubuntu:16.04

# Install prerequisites
RUN apt-get -q update && apt-get install -y -qq \
  git \
  curl \
  gcc \
  make \
#  build-essential \
  sudo \
  apt-utils \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Install Node.js
RUN curl -s https://deb.nodesource.com/setup_8.x | sudo -E bash - \
	&& apt-get install -y -q nodejs \
	&& apt-get clean \
  	&& rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir -p /usr/src/app
WORKDIR /user/src/app

CMD ["bash"]
