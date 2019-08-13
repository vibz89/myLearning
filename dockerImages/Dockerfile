FROM ubuntu

RUN apt-get update && \
	 apt-get install nginx -y && \
	 apt-get install htop

#specify the actual working directory where we have to place our static file (here of nginx)
WORKDIR /var/www/html

#copy the file
COPY index.html index.html

#create the volume
VOLUME ["/var/www/html"]

#expose the port
EXPOSE 80

#specify the command which will keep it alive
CMD ["nginx","-g","daemon off;"]