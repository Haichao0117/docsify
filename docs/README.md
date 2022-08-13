# 自学笔记

> An awesome project.





## 前端



### HTML（**H**yper **T**ext **M**arkup **L**anguage）

超文本标记语言



### CSS（）



### JavaScript（）



## 后端









## 数据库

### 安装







* 数据库安装问题记录：
  * 数据库安装时设置密码强度为中，简单密码无法设置`SHOW VARIABLES LIKE 'validate_password%';` 显示密码强度
    
    * ```
      +--------------------------------------+--------+
      | Variable_name                        | Value  |
      +--------------------------------------+--------+
      | validate_password.check_user_name    | ON     |
      | validate_password.dictionary_file    |        |
      | validate_password.length             | 8      |
      | validate_password.mixed_case_count   | 1      |
      | validate_password.number_count       | 1      |
      | validate_password.policy             | MEDIUM |
      | validate_password.special_char_count | 1      |
      +--------------------------------------+--------+
      ```
    
  * `set global validate_password.policy=LOW;` 修改密码强度
  
  * 然后就可以创建用户了`create user 'whc'@'%' identified by 'haichao0117';`
  
  * 查看用户权限` show grant for 'whc'@'%';`
  
    * ```
      +---------------------------------+
      | Grants for whc@%                |
      +---------------------------------+
      | GRANT USAGE ON *.* TO `whc`@`%` |
      +---------------------------------+
      ```
  
  * 赋权限（全部权限）`grant all on *.* to 'whc'@'%'  with grant option;`
  
  * 远程访问不通，需要修改MySQL配置文件，允许远程访问`sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf` ，在**bind-address**中添加远程访问数据库的ip，用`,`分隔（*此处使用192.168.X.X，重启提示参数错误*）；设置`0.0.0.0`允许任意ip访问。然后重启MySQL`sudo service mysql restart`

