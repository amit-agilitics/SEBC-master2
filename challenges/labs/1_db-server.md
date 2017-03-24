Steps followed
===============

```


only on mysql place

sudo yum install mysql-server -y
sudo service mysqld start


On all servers

sh clustercmd.sh  sudo yum install mysql -y

on MYSQL Server

 sudo /usr/bin/mysql_secure_installation
 change the password

 mysql -u root -p

 login with new password

 mysql> create database scm DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on scm.* TO 'cloudera-scm'@'%' IDENTIFIED BY 'cloudera-scm';
Query OK, 0 rows affected (0.00 sec)

mysql> create database rman DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman';
Query OK, 0 rows affected (0.00 sec)

mysql> create database hive DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on hive.* TO 'hive'@'%' IDENTIFIED BY 'hive';
Query OK, 0 rows affected (0.00 sec)

mysql> create database hue DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on hue.* to 'hue'@'%' IDENTIFIED BY 'hue';
crQuery OK, 0 rows affected (0.00 sec)

mysql> create database oozie DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

mysql> grant all on oozie.* to 'oozie'@'%' IDENTIFIED BY 'oozie';
Query OK, 0 rows affected (0.00 sec)

mysql> create database sentry DEFAULT CHARACTER SET utf8;
grant allQuery OK, 1 row affected (0.00 sec)

mysql> grant all on sentry.* to 'sentry'@'%' IDENTIFIED BY 'sentry';
Query OK, 0 rows affected (0.00 sec)

create database metastore DEFAULT CHARACTER SET utf8;
grant all on metastore.* to 'hue'@'%' IDENTIFIED BY 'hue';

sh clustercmd.sh mysql --version

install mysql connector 
=====================

sh clustercmd.sh wget http://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.40.tar.gz
sh clustercmd.sh tar -zxvf mysql-connector-java-5.1.40.tar.gz
sh clustercmd.sh sudo mkdir /usr/share/java
sh clustercmd.sh  sudo cp mysql-connector-java-5.1.40/mysql-connector-java-5.1.40-bin.jar /usr/share/java/mysql-connector-java.jar
sh clustercmd.sh ls /usr/share/java


Hostname of DB Node
====================

```
[centos@ip-172-31-9-165 ~]$ hostname -f
ip-172-31-9-165.ap-southeast-1.compute.internal
[centos@ip-172-31-9-165 ~]$
````


Hostname of DB Version
====================
````
[centos@ip-172-31-9-165 ~]$ mysql --version
mysql  Ver 14.14 Distrib 5.5.54, for Linux (x86_64) using readline 5.1



Database schema created
========================

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
10 rows in set (0.00 sec)
