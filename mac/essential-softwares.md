Install Java, Maven

Download File: https://www.oracle.com/java/technologies/downloads/#java8
Install it

Download Maven: https://maven.apache.org/download.cgi
Extract it

Set Path Variables and Export Them:

Create a new file - touch ~/.bash_profile
                    vi ~/.bash_profile
                    
Add Below Contents to the file:        

export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_301.jdk/Contents/Home/;
export PATH=$PATH:$JAVA_HOME;
export PATH=$PATH:/Users/akg/Downloads/apache-maven-3.8.2/bin;

Save the File
Run the File: source ~/.bash_profile

Get Set GO
