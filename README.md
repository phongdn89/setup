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
