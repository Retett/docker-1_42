FROM kstaken/apache2

MAINTAINER ayavorsk

RUN apt-get update -y 
RUN apt-get install php5 libapache2-mod-php5 php5-mysql php5-cli  -y 
RUN apt-get clean -y
RUN rm -rf /var/lib/apt/lists/*

EXPOSE 3030

CMD ["/usr/sbin/apache2"]