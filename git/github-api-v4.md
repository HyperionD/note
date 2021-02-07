

# github-api-v4

 

获取目录下文件及文件夹

 

```

query {

    repository(name: "vnote", owner: "HyperionD") {

    object(expression: "master:") {

      ... on Tree {

        entries {

          name

          type

          mode

        }

      }

    }

  }

}

```

 

获取文件内容

 

```

query {

    repository(name: "vnote", owner: "HyperionD") {

    object(expression: "master:hyperion/IT/CentOS/git-http-server.md") {

      ... on Blob {

        text

      }

    }

  }

}

```





