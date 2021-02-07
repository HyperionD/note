

# samba相关

 

1. 列出服务器上可用共享

 

```

smbclient -L 192.168.1.100 -U%

```

 

2.  挂载共享

 

```

# mount -t cifs //SERVER/sharename /mnt/mountpoint -o user=username,password=password

```





