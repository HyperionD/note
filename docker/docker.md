

# docker

 

 

1.  列出所有容器ID

 

```

# docker ps -aq

```

 

2. 查看所有运行或者不运行容器

 

```

# docker ps -a

```

 

3. 停止容器

 

```

# docker stop <docker name>/<docker id>

```

 

4. 删除容器

 

```

# docker rm <docker name>/<docker id>

```

 

5. 将容器导出为镜像

 

```

# docker export furious_bell > /home/myubuntu-export-1204.tar

```

 

6. 进入docker容器

 

```

# docker exec -it <docker_name>/<docker_id> bash

```





