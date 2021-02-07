

# 使用docker部署oracle

 

1. 下载oracle的docker-images

 

```

git clone https://github.com/oracle/docker-images.git

```

 

2. 将下载的oracle安装包放到相应版本目录

 

```

docker-images/OracleDatabase/SingleInstance/dockerfile/12.1.0.2

```

 

3. 运行构建镜像脚本

 

```

# ./buildDockerImage.sh -v 12.1.0.2 -e

```

 

4. 运行镜像

 

```

 docker run --name oracle -p 1521:1521 -p 5500:5500 -d -e ORACLE_SID=orcl -e ORACLE_PWD=dongjj oracle/database:12.1.0.2-ee

 ```





