docker-compose up -d  
docker exec -it -u root bitrix-app bash  
docker-compose down  
  
docker run -p 3307:3306 -t db1 -e MYSQL_ROOT_PASSWORD=root -d mysql:5.7  
mysql --host=127.0.0.1 --port=3307 -u root -p  
  
*Delete all containers*  
docker rm $(docker ps -aq)  
*Delete all images*  
docker rmi $(docker images -q)  
*Delete all untagged images*  
docker rmi $(docker images -q --filter "dangling=true")  
*Remove all volumes*  
docker volume rm $(docker volume ls -qf)  
  
Для базы данных вместо localhost написать bitrrix-db  
 
