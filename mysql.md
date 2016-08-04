MySql
===

```
> SHOW DATABASES;
> CREATE DATABASE db_name;
> DROP DATABASE db_name;
> CREATE USER user@localhost IDENTIFIED BY 'user';
> GRANT ALL PRIVILEGES ON dbname.* TO user@localhost;
> FLUSH PRIVILEGES;
> EXIT
```

```
$ mysql -h hostname -u user -pXXX database < dump_file
$ mysqldump -u user -pXXX --databases db_name -h host > dumpfile.sql
```
