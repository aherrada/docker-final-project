
docker run -d --name mysql -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_DATABASE=homestead -e MYSQL_USER=homestead -e MYSQL_PASSWORD=secret mysql:5.6

docker run --name web --link mysql:mysql -d -p 8081:80 -v /home/aherrada/Documents/docker\ trainning/docker-final-project/worldapi:/opt/www/worldapi web:1.0
