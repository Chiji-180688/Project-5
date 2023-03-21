# Documentation of Project 5

`created server1 - server`
`created server2 - client`
`packages updated`
![apt update](./Images-5/client%20apt%20update.PNG)
`installed mysql server on server and client`
![mysql installed on server](./Images-5/mysql%20client%20installed.PNG)
`created new inbound rule - port 3306 on server`
`restricted connection to client only`
`sudo mysql`
![sudo mysql](./Images-5/sudo%20mysql.PNG)
`CREATE USER 'remote_user'@'%' IDENTIFIED WITH mysql_native_password BY 'new_password';`
`CREATE DATABASE test_db;`
`GRANT ALL ON test_db.* TO 'remote_user'@'%' WITH GRANT OPTION;`
`FLUSH PRIVILEGES;`
![running security script on server](./Images-5/Running%20security%20script%20on%20mysql%20server.PNG)
`sudo mysql_secure_installation`
![secure installation](./Images-5/mysql%20secure%20installation.PNG)
`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`
![configuring server to allow connections from host](./Images-5/configuring%20mysql%20server%20to%20allow%20access%20to%20remote%20user.PNG)
`sudo mysql -u remote_user -h 172.31.6.141 -p`
![successfully connected to host from client](./Images-5/successfully%20connected%20to%20host%20from%20client.PNG)
`show databases;`
![sql query](./Images-5/sql%20query%20successfully%20performed.PNG)