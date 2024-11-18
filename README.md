This is cammand line in Linux
This is command line in Linux

1. Fisrt install mysql server client, Chỉ cài 1 lần duy nhất, nhớ start

sudo apt update
sudo apt install mysql-server mysql-client -y
sudo service mysql start

2. Run mysql: 
sudo mysql

Output: 

@Lk13Antkoo ➜ /workspaces/MySQL (main) $ sudo mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 12
Server version: 8.0.40-0ubuntu0.20.04.1 (Ubuntu)

Copyright (c) 2000, 2024, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

3. Set password:

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '@Phamhoangan21';

4. Create databse 

CREATE DATABASE budapest_demo

5. Download database 

UPDATE user SET authentication_string=PASSWORD('phamhoangan21') WHERE User='root' AND Host='localhost';

UPDATE user SET plugin='mysql_native_password' WHERE User='root' AND Host='localhost';
FLUSH PRIVILEGES
