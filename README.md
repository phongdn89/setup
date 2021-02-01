# Format readme.md github
https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax
# Setup Java
https://www.javahelps.com/2015/03/install-oracle-jdk-in-ubuntu.html

* Step 1: download java to usr/java/

* Step 2: sua bien moi truong : 
$: sudo nano /etc/environment

PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/java/jdk1.8.0_221/bin:/usr/java/jdk1.8.0_221/db/bin:/usr/java/jdk1.8.0_221/jre/bin"
J2SDKDIR="/usr/java/jdk1.8.0_221"
J2REDIR="/usr/java/jdk1.8.0_221/jre"
JAVA_HOME="/usr/java/jdk1.8.0_221"
DERBY_HOME="/usr/java/jdk1.8.0_221/db"

* Step 3: Enter the following commands to inform the system about the Java's location. Depending on your JDK version, the paths can be different.

sudo update-alternatives --install "/usr/bin/java" "java" "/usr/java/jdk1.8.0_221/bin/java" 0

sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/java/jdk1.8.0_221/bin/javac" 0

sudo update-alternatives --set java /usr/java/jdk1.8.0_221/bin/java

sudo update-alternatives --set javac /usr/java/jdk1.8.0_221/bin/javac

* Step 4: To verify the setup enter the following commands and make sure that they print the location of java and javac as you have provided in the previous step.

update-alternatives --list java

update-alternatives --list javac

# Switch all version Java on Ubuntu
https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-18-04
https://dzone.com/articles/installing-openjdk-11-on-ubuntu-1804-for-real

# Setup maven
https://www.javahelps.com/2017/10/install-apache-maven-on-linux.html

# Problem password mysql 5.7 first time CentOS 7
* Open & Edit /etc/my.cnf or /etc/mysql/my.cnf, depending on your distro.
* Add skip-grant-tables under [mysqld]
* Restart Mysql
* You should be able to login to mysql now using the below command mysql -u root -p
* Run mysql> flush privileges;
* Set new password by ALTER USER 'root'@'localhost' IDENTIFIED BY 'NewPassword';
* Go back to /etc/my.cnf and remove/comment skip-grant-tables
* Restart Mysql
* Now you will be able to login with the new password mysql -u root -p
