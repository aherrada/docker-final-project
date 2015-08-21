
docker run --name mysql -e MYSQL_DB_HOST: localhost -e MYSQL_DB_DATABASE: homestead -e MYSQL_DB_USERNAME: homestead -e MYSQL_DB_PASSWORD: secret -d mysql:5.6

docker run --name web --link mysql:mysql -d -p 8081:80 -v /opt/docker/worldapi:/opt/www/worldapi php-link:1.0
