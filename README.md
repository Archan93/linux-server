# Linux-Server-Configuration

Take a baseline installation of a Linux distribution on a virtual machine
and prepare it to host web applications, to include installing updates,
securing it from a number of attack vectors and installing/configuring web and database servers.

##  Go to http://52.27.63.192 to check the app.

## Steps get it done.

### 1. Launch your Virtual Machine with your Udacity account

### 2. Follow the instructions provided to SSH into your server

### 3. Create a new user named grader

### 4. Give the grader the permission to sudo
		$ visudo
		-- Add "grader ALL=(ALL:ALL) ALL".
	
### 5. Update all currently installed packages

### 6.  -- Open sshd_config file.
		-- Change Port 22 to 2200.
		-- Change "PermitRootLogin from without-password to no".
		-- Add "UseDNS no".
		-- Add "AllowUsers grader".
		-- Close the file and restart ssh service.
		-- Create a SSH key and login to new user.

### 7. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123) 
		-- Turn UFW on with the default set of rules  
		-- Allow incoming TCP packets on port 2200 (SSH)  
		-- Allow incoming TCP packets on port 80 (HTTP)
		-- Allow incoming UDP packets on port 123 (NTP)  

### 8. Configure the local timezone to UTC
		-- Open the timezone selection dialogue-box  
		-- Then chose 'None of the above', then UTC.

### 9. Install and configure Apache to serve a Python mod_wsgi application
		-- Install Apache web server
		-- Install the helper package "python-setuptools"  
		-- Restart the Apache server for mod_wsgi to load 

### 10. Install and configure PostgreSQL
	-- Install PostgreSQL:  
	-- Check that no remote connections are allowed (default)  
	-- Create needed linux user for psql  
	-- Change to default user postgres:  
	-- Connect to the system  
	-- Add postgre user with password:  
	-- Create database  
	-- Connect to the database catalog
	-- Revoke all rights  
	-- Grant only access to the catalog role  
	-- Exit out of PostgreSQl and the postgres user  
	-- Create postgreSQL database schema  		

### 11. Install git, clone and setup your Catalog App project
	-- Install and configure git
    -- Install python-dev
	-- Enable wsgi mod
	-- Install Flask
	-- Install pip Installer and install virtualenv
	-- Configure and Enable a New Virtual Host (you will need to create catalog.conf)
	-- Enable the virtual host  
	-- Create the .wsgi File and Restart Apache 
    -- Clone github repository and it inaccessible
	-- Install httplib2, oauth2client, sqlalchemy, python-psycopg2

#### Restart Apache 

### Get OAuth-Logins Working
	-- Go to the project on the Developer Console
	-- Navigate to APIs & auth > Credentials > Edit Settings
	-- add your host name and public IP-address to your Authorized JavaScript origins
	   and your host name + oauth2callback to Authorized redirect

