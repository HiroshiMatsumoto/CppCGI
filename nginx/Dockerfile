FROM nginx:latest

# RUN cat /etc/os-release
RUN apt-get -y update
RUN apt-get -y upgrade

RUN apt-get -y install libfcgi-dev spawn-fcgi curl g++
# RUN apt-get install nginx

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
