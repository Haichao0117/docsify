# 数据库知识

记录数据库基础知识及常用操作。

## SQL



## 数据库操作



### 数据库操作

#### 修改数据库密码强度设置

* `SHOW VARIABLES LIKE 'validate_password%';` 显示密码强度

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

#### 创建用户并赋予权限

* 创建用户了`create user 'whc'@'%' identified by 'haichao0117';`

* 查看用户权限` show grant for 'whc'@'%';`

  * ```
    +---------------------------------+
    | Grants for whc@%                |
    +---------------------------------+
    | GRANT USAGE ON *.* TO `whc`@`%` |
    +---------------------------------+
    ```

  * 赋权限（全部权限）`grant all on *.* to 'whc'@'%'  with grant option;`

#### 数据库远程访问

* 远程访问不通，需要修改MySQL配置文件，允许远程访问`sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf` ，在**bind-address**中添加远程访问数据库的ip，用`,`分隔（*此处使用192.168.X.X，重启提示参数错误*）；设置`0.0.0.0`允许任意ip访问。然后重启MySQL`sudo service mysql restart`