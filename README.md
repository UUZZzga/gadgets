## SonarQube

启动命令
```
docker-compose -f "sonarqube\docker-compose.yml" up -d --build
```

在windows下可能会出现报错

```
max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```

[解决方案](sonarqube/%E6%8A%A5%E9%94%99%E8%A7%A3%E5%86%B3.md)

## ZooKeeper+Kafka

启动命令

```
docker-compose -f "zk_kafka\docker-compose.yml" up -d --build
```
