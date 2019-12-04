# mysql远程连接

## 关闭远程连接

1. 使用root用户登录到数据库
2. use mysql 选择mysql数据库
3. revoke all privileges on *.* from 'root'@'%'; 撤回权限
4. delete from user where User="root" and Host="%"; 删除用户
5. flush privileges; 刷新

## 开启远程连接

1. 找到mysql的配置文件，注释或者修改掉bind-address
2. 登陆mysql给对应的账户分配权限
    - `GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password';`
3. flush privileges; 刷新
4. service mysql restart 重启mysql
