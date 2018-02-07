# CS316-AirbnbProject
Created by JiaHui Wang, JiaLei Guo, YanLin Yu, YiYi Ye, Ran Zhou, Zhaoxi Zhang

Set up instructions:
Pacakage set up under linux Ubuntu 16.04 using vagrant and VM
	1. Install Flask, WTForm, SQLAlchemy psql other package 
Database set up
	2.1 Decompress the airdb.zip files from 001 - 006 to obtain the airdb database dump file
	2.2 rename the following lines to the actual address of where you save the csv files 
		\COPY Crime FROM 'crimerate.csv' DELIMITER ',' CSV HEADER;
		\COPY House FROM 'house_new.csv' DELIMITER ',' CSV HEADER;
	2.3 create the user vagrant by 
		First login to psql by: sudo -u postgres psql in the terminal
		Second, create user "vagrant" with password: dbpasswd
		CREATE USER vagrant password "dbpasswd";
			Or, create any user you would like but remeber to change the setting in config.py
			SQLALCHEMY_DATABASE_URI = 'postgresql://YourUserName:YourPassword@localhost/airdb'
	2.4 create databse with name "airdb"
		CREATE DATABASE airdb;
	2.5 dump the .sql file into the created databased by: psql airdb < airdb.sql in the terminal
Running the website 
	3. run the app.py by: python app.py in the terminal 
Any other thing
	4. Enjoy!!!
