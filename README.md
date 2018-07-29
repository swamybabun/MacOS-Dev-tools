# mac-tools
Developer tools and commands for Mac OS

This document explains how i setup my developer enviroment with commands.

# 1) Environment Variables:

- EDIT the Bash profile

    vim  ~/.bash_profile

- Appending the new path (MySQL path) to the existing PATH

    export PATH=$PATH:/usr/local/mysql-8.0.11-macos10.13-x86_64/bin/   
    
- Echo the PATH 

    echo $PATH
    
    
# 2) MySQL Setup :

Download and install MySQL downloded from https://dev.mysql.com/downloads/mysql/.

At the end of installation, it will ask you to set username and password. Set the credentials and finish installation.
After installation, you can login to mysql command line tool and can do further work.

If suppose, it didnt ask you to enter username/password then you can reset the password with below commands and if you are unable to login to **root** user, then you can do below steps.

Open a Terminal and run below commands.

**sudo /usr/local/mysql/support-files/mysql.server stop**

**sudo ./mysqld_safe --skip-grant-tables**

Keep the current terminal running, and open a new terminal and run the below commands.

**mysql -u root**

**FLUSH PRIVILEGES;**

You can set password to your desired one with below command

**ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';**

then start the MySQL server with below command.

**sudo /usr/local/mysql/support-files/mysql.server start**
