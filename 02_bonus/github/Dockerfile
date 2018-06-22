FROM debian 

RUN apt-get update && apt-get install -y curl

# ADD weather.sh .

RUN echo "#!/bin/bash \
echo '\nWhat city would you like the weather report for?'\
read varname\
varname=$(echo $varname | sed 's/ /%20/g')\
while [ $varname != "exit" ]\
do\
	echo '\n\n'\
	curl http://wttr.in/$varname\
	echo '\n\n'\
	echo 'What city would you like the weather report for?'\
	read varname\
	varname=$(echo $varname | sed 's/ /%20/g')\
done"  > weather.sh

CMD ["sh", "weather.sh"]
