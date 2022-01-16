_Variables store information. Environment variables are available for the whole environment._
_An environment variable consists of _name=value_ pair._

**Existing Environment Variables:**
- `SHELL=/bin/bash`= default shell program, in this case bash
- `HOME=/home/nana`= current user's home directory
- `USER=nana` = currently logged in user
<!-- -->
- `printenv` = List all environment variables
- `printenv | less` = List all environment variables with less program
- `printenv [environment variable]` = Display value of given environment variable, e.g. `printenv USER`
- `printenv | grep USER` = Filter environment variables, which have 'USER' in the name
<!-- -->
- `echo $USER` = Print value of USER environment variable

**Create own Environment Variables:**
- `export DB_USERNAME=dbuser` = Set environment variable 'DB_USERNAME' with value 'dbuser'
- `export DB_PASSWORD=secretpwdvalue` = Set environment variable 'DB_PASSWORD' with value 'secretpwdvalue'
- `export DB_NAME=mydb` = Set environment variable 'DB_NAME' with value 'mydb'
- `printenv | grep DB` = Filter environment variables for 'DB' characters
- `export DB_NAME=newdbname` = Set environment variable 'DB_NAME' to new value 'newdbname'

**Delete Environment Variables:**
- `unset DB_NAME` = Delete variable with name 'DB_NAME'

**Persisting Environment Variables:**

Persisting Environment Variables with shell specific configuration file:
_Environment variables set in terminal are only available in the current terminal session._

Add environment variables to the '~/.bashrc' file or your specific shell 'rc' file. Variables set in this file are loaded whenever a bash login shell is entered.
- `export DB_USERNAME=dbuser`
- `export DB_PASSWORD=secretvl`
- `export DB_NAME=mydb`
In terminal again:
- `source ~/.bashcrc` = Load the new env vars into the current shell session

Persisting Environment Variables system wide:
- ~./bashrc = user specific
- /etc/environment = system wide, meaning all users will have access to the variables

**PATH Environment Variable:**
- `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin` = List of directories to executible files, separated by ':'. Tells the shell which directories to ssearch for the executable in response to our executed command
- `PATH=$PATH:/home/nana` = Appending /home/nana folder to the existing $PATH value

