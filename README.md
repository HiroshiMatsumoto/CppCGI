# Running C++ CGI on nginx

This is a simple docker environment for C++ CGI on nginx server.

## how to run

run docker-compose

```bash
docker-compose build
docker-compose up
```

get into nginx container

```bash
docker-compose exec nginx bash
```

compile c++ source code to cgi binary file
then, run server with spawn-fcgi command

```bash
root@XXXX:/# cd /etc/nginx/html
root@XXXX:/etc/nginx/htm# g++ sample.cpp -lfcgi++ -lfcgi -o index.cgi
root@XXXX:/etc/nginx/htm# spawn-fcgi -p 8000 -n index.cgi
```

## reference

- http://chriswu.me/blog/writing-hello-world-in-fcgi-with-c-plus-plus/
