# MacOS-DEV-tools
Developer tools and commands for Mac OS


This document contains the tools and steps for setting up developer environment. I am using **macOS High Sierra 10.13.6** operating system.  This document considers you are a newbie to the Mac Computer.

## Tools

* [Google Chrome](#google-chrome)
* [iTerm2](#iterm2)
* [Sublime Text](#sublime-text)
* [Eclipse](#eclipse)
* [Misc Section](#misc)

## Google Chrome
Download and install the most famous web browser Google Chrome from https://www.google.co.in/chrome/. Download DMG file and click on it once downloading is finished and drag&drop the Google chrome icon to Applications folder. Unmount the disc when you are done with installation.

## iTerm2
Download and install the most advanced version of terminal from https://www.iterm2.com/.

## Sublime Text
Download and install the simple and intuitive editor "sublime Text" from https://www.sublimetext.com/

## Eclipse

Download and install the Eclipse IDE from https://www.eclipse.org/downloads/


## Misc Section
### 1) Environment Variables:

- EDIT the Bash profile:

      $ vim  ~/.bash_profile

- Appending the new path (MySQL path) to the existing PATH:

      $ echo 'export PATH=$PATH:/usr/local/mysql-8.0.11-macos10.13-x86_64/bin/' >> ~/.bash_profile
    
- Echo the PATH:

      $ echo $PATH
    
    
### 2) MySQL Setup :

Download and install MySQL downloded from https://dev.mysql.com/downloads/mysql/.

At the end of installation, it will ask you to set username and password. Set the credentials and finish installation.
After installation, you can login to mysql command line tool and can do further work.

If suppose, it didnt ask you to enter username/password then you can reset the password with below commands and if you are unable to login to **root** user, then you can do below steps.

- Open a Terminal and run below commands.

      sudo /usr/local/mysql/support-files/mysql.server stop

      sudo ./mysqld_safe --skip-grant-tables

- You can set password to your desired one with below command

       ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';

- Then start the MySQL server with below command.

       sudo /usr/local/mysql/support-files/mysql.server start
