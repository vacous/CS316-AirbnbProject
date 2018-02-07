# CS316-AirbnbProject
Created by JiaHui Wang, JiaLei Guo, YanLin Yu, YiYi Ye, Ran Zhou, Zhaoxi Zhang

### Set Up Instructions:
Pacakage set up under linux Ubuntu 16.04 using vagrant and VM

* 1.1 &nbsp; Install Flask, WTForm, SQLAlchemy psql other package 

Database set up

* 2.1 &nbsp; Decompress the airdb.zip files from 001 - 006 to obtain the airdb database dump file

* 2.2 &nbsp; rename the following lines to the actual address of where you save the csv files 

>	\COPY Crime FROM 'crimerate.csv' DELIMITER ',' CSV HEADER;
    
>	\COPY House FROM 'house_new.csv' DELIMITER ',' CSV HEADER;

* 2.3 &nbsp; create the user vagrant by 
<ul>
<li>First login to psql by: sudo -u postgres psql in the terminal </li>
<li>Second, create user "vagrant" with password: dbpasswd</li>

> CREATE USER vagrant password "dbpasswd";

<li>Or, create any user you would like but remeber to change the setting in config.py</li>

> SQLALCHEMY_DATABASE_URI = 'postgresql://YourUserName:YourPassword@localhost/airdb'
</ul>

* 2.4 &nbsp; create databse with name "airdb"
>	CREATE DATABASE airdb;
 

* 2.5 &nbsp; dump the .sql file into the created databased by: psql airdb < airdb.sql in the terminal

Run the Website 

* 3.1 run the app.py by: python app.py in the terminal

<img src ="https://github.com/vacous/CS316-AirbnbProject/blob/master/DemoImages/HomePage.png?raw=true"\>

<img src ="https://github.com/vacous/CS316-AirbnbProject/blob/master/DemoImages/HostPage.png?raw=true"\>

<img src ="https://github.com/vacous/CS316-AirbnbProject/blob/master/DemoImages/RenterPage.png?raw=true"\>
