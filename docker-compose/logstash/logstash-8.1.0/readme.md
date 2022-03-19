#使用脚本
#官方文档：https://www.elastic.co/guide/en/logstash/current/docker-config.html

docker pull docker.elastic.co/logstash/logstash:8.1.0

docker cp mylogstash:/usr/share/logstash/config/ .

docker run --name mylogstash --rm -it -v /Users/liuchao58/Mydocker/renrenche/docker-master/docker-compose/logstash/logstash-8.1.0/config/:/usr/share/logstash/config/ -v  /Users/liuchao58/Mydocker/renrenche/docker-master/docker-compose/logstash/logstash-8.1.0/ca/ca.crt:/etc/logstash/config/certs/ca.crt  docker.elastic.co/logstash/logstash:8.1.0


docker stop mylogstash

