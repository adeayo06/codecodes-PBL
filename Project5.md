## Client/Server Architecture Using a Mysql Relational Database Management System

Client-Server architecture describe the relationship between two or more connectecd computer sharing data across the network. The computer that request for data is known as the client while the one that processes the request is known as the server.

To demonstrate Client-Server architecture we will be using two EC2 instance with mysql-server and mysql-client respectively.

- Create and configure two Linux-based virtual servers (EC2 instances in AWS).

- Name one instance Mysql-server the other Mysql-client

- On mysql server Linux Server install MySQL Server software.

- On mysql client Linux Server install MySQL Client software.

#### MySql EC2 instances (Client and Server) on AWS
![EC2 servers](https://user-images.githubusercontent.com/114569323/198238959-3b147853-611c-4313-b8e2-8b0f85f45844.png)

#### MySql Server installation
![MySql Server installation](https://user-images.githubusercontent.com/114569323/198240177-1e10c5dc-164b-4843-83f9-0764bc6ef67b.png)

- Open port 3306 on Mysql-server allow for connection. Both server can communicate using private IPs since they belong to the same subnet

- Change bind-address on Mysql-server to allow for connection from any IP address. Set the bind-address to 0.0.0.0 using the command below:

  `sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`
  
- From mysql client Linux Server connect remotely to mysql server Database Engine without using SSH. You must use the mysql utility to perform this action.

- Check that you have successfully connected to a remote MySQL server and can perform SQL queries. You should something similar to the screenshot below:

#### Remote access to the MySql server from the Client Server
![remote access to mysql](https://user-images.githubusercontent.com/114569323/198239571-5152d972-4876-40e8-9e1f-9560331ab3a3.png)
