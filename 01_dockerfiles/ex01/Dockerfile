FROM debian
MAINTAINER mgill

WORKDIR home/teamspeak
RUN apt-get update && apt-get install bzip2 wget -y \
	&& wget http://dl.4players.de/ts/releases/3.2.0/teamspeak3-server_linux_amd64-3.2.0.tar.bz2 \
	&& bunzip2 teamspeak3-server_linux_amd64-3.2.0.tar.bz2 \
	&& tar -xvf teamspeak3-server_linux_amd64-3.2.0.tar \
	&& touch teamspeak3-server_linux_amd64/.ts3server_license_accepted \
	&& useradd ts3

EXPOSE 9987/udp 30033 10011
# CMD ["bash"]
CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# https://www.unixblogger.com/2017/11/08/setup-a-teamspeak-3-server-on-linux-ubuntu-debian/
# to download and extract the server software we need some additional software:
# 	 a download manger (wget) and the utility to extract the compromised server software (bzip2)
