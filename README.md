# MariaDB-for-WordPress
MariaDB configuration into Linux VPS for WordPress installation

#install MaraiDB into Centos 7 

`yum update`  
`yum install mariadb mariadb-server` 
`systemctl enable mariadb`  
`systemctl start mariadb`  
`systemctl stop mariadb`  
`systemctl restart mariadb`  

# Secure your MariaDB installation 
`mysql_secure_installation`  

# Create mysql Database and user
`mysql -u root -p`  provide here root mysql root password.     
`CREATE DATABASE wpdb;`  
`CREATE USER wpuser@localhost;`   
`SET PASSWORD FOR wpuser@localhost= PASSWORD("password");`    
`GRANT ALL PRIVILEGES ON wpdb.* TO wpuser@localhost IDENTIFIED BY 'password';`     
`FLUSH PRIVILEGES;`    
`exit`  

# Tune MariaDB

`yum install bc`  
`wget http://www.day32.com/MySQL/tuning-primer.sh`  
`chmod u+x tuning-primer.sh`  

`./tuning-primer.sh`  














