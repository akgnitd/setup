# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Java, Maven and Set Path Variables

### Java
Download File: https://www.oracle.com/java/technologies/downloads/#java8
Install it

### Maven
Download Maven: https://maven.apache.org/download.cgi
Extract it

### Set Path Variables and Export Them:

Create a new file - touch ~/.bash_profile
                    vi ~/.bash_profile
                    
Add Below Contents to the file:        

export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_301.jdk/Contents/Home/;
export PATH=$PATH:$JAVA_HOME;
export PATH=$PATH:/Users/akg/Downloads/apache-maven-3.8.2/bin;

Save the File
Run the File: source ~/.bash_profile

# Install Python3, pip3

### Python3

Download and Install Python3 from: https://www.python.org/downloads/macos/

### Pip3
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py

# Install and Setup Postgres
brew update
brew doctor
brew install postgres

## Start Postgres Server
postgres -D /usr/local/var/postgres

## Connect to Postgres Server
sudo psql -U akg postgres

where, akg -> user,
postgres -> default database

## Create New User in Postgres
create user akg with encrypted password 'admin';

## Grant Privileges
grant all privileges on database proddb to akg;

## List Users
\du

## Drop User
DROP OWNED BY akg;
DROP user akg;

## Change User Password
alter user akg with password 'mylife';
