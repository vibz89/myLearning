FROM ubuntu

RUN apt-get update \
	&& apt-get install nginx -y \
	&& apt-get install htop \
	&& apt-get install wget -y \
	&& apt-get install -y php7.0
	
	

# creating a folder 
RUN	mkdir /var/downloads && \
    wget -O /var/downloads/master.zip https://github.com/dockerfile/nginx/archive/master.zip


#Copying customised default to update port for nginx
COPY default /etc/nginx/sites-enabled/default

#specify the working directory 
WORKDIR /var/www/html

#ADD Folder
COPY src /var/www/html/src/

#create the volume
VOLUME ["/var/www/html"]

#expose the port
EXPOSE 81

#specify the command which will keep it alive
CMD ["nginx","-g","daemon off;"]