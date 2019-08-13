FROM ubuntu

RUN apt-get update \
	&& apt-get install nginx -y \
	&& apt-get install htop 
	

#specify the working directory 
WORKDIR /var/www/html

RUN mkdir mkdir /var/www/html/app
COPY app /var/www/html/app

#create the volume
VOLUME ["/var/www/html"]

#expose the port
EXPOSE 80

#specify the command which will keep it alive
CMD ["nginx","-g","daemon off;"]