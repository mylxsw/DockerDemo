stop:
	docker stop nginx_server
	docker stop phpfpm
	docker rm nginx_server
	docker rm phpfpm

run:
	docker run --name phpfpm -d -v /Users/mylxsw/codes/php:/app php:5.6-fpm
	docker run --name nginx_server -d -p 80:80 --link phpfpm:phpfpm -v /Users/mylxsw/Dockers/nginx-php/nginx.conf:/etc/nginx/nginx.conf --volumes-from phpfpm  nginx
	docker ps

log:
	docker logs -f nginx_server
