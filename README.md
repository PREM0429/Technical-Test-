## Login System with Python Flask and MySQL

### Requirements(Minimum)

Download and install Python, I am using Python 3.9, make sure to check the box Add Python to PATH on the installation setup screen. </p>
Download and install MySQL Community Server and MySQL Workbench, you can skip this step if you already have a MySQL server set up. </p>

**Major operations handled**

main.py — This will be our main project file, which will contain all our Python code (Routes, MySQL connection, validation, etc.).
index.html — The login form template created with HTML5 and CSS3.
register.html — The registration form template created with HTML5 and CSS3.
home.html — The home template which is restricted to logged-in users.
profile.html — The profile template which is restricted to logged-in users. The user's details will be populated on this page.
layout.html — The layout template for the home and profile templates.
contact.html - The layout template for the contact page.
style.css — The CSS3 stylesheet for our login and registration system.


### Requirements ,Packages used and Installation
Download and install Python, for this  I'll be using Python 3.7.2, make sure to check the box Add Python to PATH on the installation setup screen

### 2. Create the database and table 

```sql
-- Create the  database named "loginapp"
CREATE DATABASE pythonlogin;


-- Switch to 'loginapp' database; 
USE pythonlogin; 


-- Create 'account' table with id, username,email, password columns. 
CREATE DATABASE IF NOT EXISTS `pythonlogin` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `pythonlogin`;

CREATE TABLE IF NOT EXISTS `accounts` (
	`id` int(11) NOT NULL AUTO_INCREMENT,
  	`username` varchar(50) NOT NULL,
  	`password` varchar(255) NOT NULL,
  	`email` varchar(100) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

INSERT INTO `accounts` (`id`, `username`, `password`, `email`) VALUES (1, 'test', 'test', 'test@test.com'); 
```

### 6. Run the application 
set FLASK_APP=main.py
set FLASK_DEBUG=1
flask run
