# MacOS-DEV-tools
Developer tools and commands for Mac OS


This document contains the tools and steps for setting up developer environment. I am using **macOS High Sierra 10.13.6** operating system. This document considers you are a newbie to the Mac Computer.

## Tools

* [Google Chrome](#google-chrome)
* [iTerm2](#iterm2)
* [Sublime Text](#sublime-text)
* [Eclipse](#eclipse)
* [MySQL](#mysql)
* [Environment Variables](#environment-variables)

## Google Chrome
Download and install the most famous web browser Google Chrome from [Download Google Chrome](https://www.google.co.in/chrome/). Download DMG file and click on it once downloading is finished and then drag&drop the Google chrome icon to Applications folder. Unmount the disc, when you are done with installation.

## iTerm2
Download and install the most advanced version of terminal from [Download iTerm2](https://www.iterm2.com/).

## Sublime Text
Download and install the simple and intuitive editor "sublime Text" from [Download SublimeText](https://www.sublimetext.com/).

## Eclipse
Download and install the Eclipse IDE from [Download Eclipse](https://www.eclipse.org/downloads/).
Go to Eclipse marketplace and install the following plugins, if required -
      [SVN](http://marketplace.eclipse.org/content/subversive-svn-team-provider)
            (and then Go to Eclipse-> Preferences -> Team -> SVN -> SVN Connector -> SVNKit ==> select and install.),
      [Themes](http://marketplace.eclipse.org/content/darkest-dark-theme-devstyle),
      [Terminal](http://marketplace.eclipse.org/content/tm-terminal),
      [SonarLint](http://marketplace.eclipse.org/content/sonarlint),
      [Jetty Server](http://marketplace.eclipse.org/content/run-jetty-run),
      [PyDEV Tools for Python](http://marketplace.eclipse.org/content/pydev-python-ide-eclipse),
      [Emma Code Coverage](http://marketplace.eclipse.org/content/eclemma-java-code-coverage),
      [DBWeaver- DB Connector Plugin](http://marketplace.eclipse.org/content/dbeaver)
      
## MySQL
Download and install MySQL from [Download MySQL Server](https://dev.mysql.com/downloads/mysql/).

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

## Environment Variables
If you wish to append a new software path to the existing PATH variable, below are the steps.
- EDIT the Bash profile:

      $ vim  ~/.bash_profile

- Appending the new path (MySQL path) to the existing PATH:

      $ echo 'export PATH=$PATH:/usr/local/mysql-8.0.11-macos10.13-x86_64/bin/' >> ~/.bash_profile
    
- Echo the PATH:

      $ echo $PATH

