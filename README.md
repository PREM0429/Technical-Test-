# Login System with Python Flask and MySQL

## Requirements (Minimum)

1. **Python:**
   - Download and install Python. Python 3.9 is recommended. Make sure to check the box "Add Python to PATH" during installation.

2. **MySQL:**
   - Download and install MySQL Community Server and MySQL Workbench. Skip this step if you already have a MySQL server set up.

## Major Operations Handled

- **main.py:**
  - Main project file containing all Python code (Routes, MySQL connection, validation, etc.).

- **index.html:**
  - Login form template created with HTML5 and CSS3.

- **register.html:**
  - Registration form template created with HTML5 and CSS3.

- **home.html:**
  - Home template restricted to logged-in users.

- **profile.html:**
  - Profile template restricted to logged-in users. User details are populated on this page.

- **layout.html:**
  - Layout template for the home and profile templates.

- **contact.html:**
  - Layout template for the contact page.

- **style.css:**
  - CSS3 stylesheet for the login and registration system.

## Requirements, Packages Used, and Installation

1. **Python:**
   - Download and install Python. Python 3.7.2 is used in this project. Check the box "Add Python to PATH" during installation.

2. **Packages:**
   - Make sure to install required packages. You can use the following command:
     ```bash
     pip install -r requirements.txt
     ```

## Create the Database and Table

```sql
-- Create the database named "loginapp"
CREATE DATABASE pythonlogin;

-- Switch to 'loginapp' database;
USE pythonlogin;

-- Create 'account' table with id, username, email, password columns.
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


## Run the application 
```
set FLASK_APP=main.py
set FLASK_DEBUG=1
flask run
