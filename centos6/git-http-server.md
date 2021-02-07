# CentOS6 配置http协议的git服务端

1.  安装软件

```

# yum install httpd git

```

2. 创建git裸仓库

```

# mkdir /repos

# cd /repos

# git init --bare test.git

```

3. 将git仓库文件夹用户更改为apache

```

# chown -R apache:apache /repos

```

4. 创建git验证账户

```

# htpasswd -m -c /etc/httpd/conf.d/git-team.htpasswd hyperion

# 如果第一个账号里有了-c其他账号要去掉-c参数

```

5. 更改git-team.htpasswd文件所有者及权限

```

# chown apache:apache /etc/httpd/conf.d/git-team.htpasswd

# chmod 640 /etc/httpd/conf.d/git-team.htpasswd

```

6.  更改/etc/httpd/conf/httpd.conf

```

# 在文件最后加入

<VirtualHost *:80>

        ServerName git.gitServer.com

        SetEnv GIT_HTTP_EXPORT_ALL

        SetEnv GIT_PROJECT_ROOT /home/gitServer

        ScriptAlias /git/ /usr/libexec/git-core/git-http-backend/

        <Location />

                AuthType Basic

                AuthName "Git"

                AuthUserFile /etc/httpd/conf.d/git-team.htpasswd

                Require valid-user

        </Location>

</VirtualHost>

```

7. 开机启动

```

chkconfig httpd on

```
