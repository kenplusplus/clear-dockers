Nigix
=======
This provides a Clear Linux* container OS based Nigix as microservice.

Build
-----
```
docker build -t bluewish/nginx
```

Or just pull it from Dockerhub
---------------------------
```
docker pull bluewish/nginx
```

Start MariaDB Container
-----------------------
```
YOUR_HOST=`hostname -f`
docker run --name nginx -p 80:80/tcp -d bluewish/nginx
```