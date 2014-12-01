PHP Nginx
======================

Enable port 80

Serves web pages out of /var/www

From Docker Index
```
docker pull usertaken/nginx-php
```

Build Yourself
```
docker build --rm -t usertaken/nginx-php github.com/UserTaken/docker-nginx-php
```

Run Example
```
docker run -d -p 80:80 -v /tmp/website:/var/www usertaken/nginx-php
```
