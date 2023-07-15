# STEP 2 - Installing MySQL
Now that the server is up and running, it's time to install the Database Management System (DBMS) to store and manage data. MySQL is the tool of choice.

Use `apt` again to install the software:
```
sudo apt install mysql-server
```
When Y when prompted to confirm installation.

When installation is finished, log into the MySQL console:
```
sudo mysql
```

This connect to the MySQL server as the admin database user root. This is how it should look:
```
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.22-0ubuntu0.20.04.3 (Ubuntu)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```
For security purposes it's recommended to run the following script. It removes insecure default settings and locks down access to the database system. The script goes as follows:
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```
Exit the MySQL shell with the following command:
```
mysql> exit
```
Run the interactive script by running:
```
$ sudo mysql_secure_installation
```

VALIDATE PASSWORD PLUGIN will appear and ask if you want to configure it. I chose not to but it's really matter of preference. It's safe to leave it disabled but passwords should always be strong & unique.

I press "ENTER" key at each prompt. It will prompt to change root password, remove anonymous users, disable root logins, and the new rules that MySQL immediately applies. 

Now issue the following command to test if able to log in to the MySQL:
```
sudo mysql -p
```
The -p flag in this command will prompt for the password after changing the root password be used.

To exit MySQL, type:
```
mysql> exit
```

The MySQL server is installed and secured. Next step will cover the installation of PHP, the last component of the LEMP stack.







