FROM debian
MAINTAINER nandu
RUN apt-get -y update && apt-get -y install apache2 net-tools
RUN mkdir -p  /var/www/html
RUN echo "<h1>Lakshmi reddy's webserver </h1>" > /var/www/html/index.html
RUN echo '<pre style="background-color: lightblue;">' >> /var/www/html/index.html 
RUN echo "`ifconfig`</pre>" >> /var/www/html/index.html
RUN echo "ServerName `hostname -I`" >> /etc/apache2/apache2.conf
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]
