FROM ubuntu:16.04
MAINTAINER mgill

RUN apt-get update -q \
	&& DEBIAN_FRONTEND=noninteractive apt-get install -yq --no-install-recommends \
	curl \
	openssh-server \
	ca-certificates \
	postfix \
	sed \
	vim \
	systemd

WORKDIR /

RUN curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash

#RUN bash script.deb.sh

RUN apt-get update && apt-get install -yq gitlab-ce
#RUN apt-get update && EXTERNAL_URL="http://192.168.99.100" apt-get install -yq gitlab-ce

EXPOSE 22 80

# RUN cd ./etc/gitlab/
# RUN sed -i 's/^external_url .*$/external_url '192.168.99.100'/' gitlab.rb
# RUN	gitlab-ctl reconfigure && gitlab-ctl restart
# CMD [ "bash" ]

# sed '0,/http://gitlab.example.com/{s /192.168.99.100/}' gitlab.rb

# sed '/^#/!s/gitlab.example.com/192.168.99.100/' gitlab.rb


# https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/common_installation_problems/README.md#reconfigure-freezes-at-ruby_blocksupervise_redis_sleep-action-run
