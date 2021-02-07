```sql
# 查看当前密码安全策略
mysql> show variables like 'validate_password%';

# 降低密码安全策略
mysql> set global validate_password.policy=0;
mysql> set global validate_password.length=4;
mysql> exit;
```


