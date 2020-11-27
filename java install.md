
### User add in web server and configuration
```shell
	java -version
	find /usr/lib/jvm/java-1.8* | head -n 3
	/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.191.b12-1.el7_6.x86_64
	
	vi .bash_profile
	--
	# User specific environment and startup programs
		JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.265.b01-0.el8_2.x86_64
		PATH=$PATH:$JAVA_HOME:$HOME/bin

		export PATH

	--
	
    source ~/.bash_profile
    echo $JAVA_HOME
  


```


sudo vi /etc/profile.d/path.sh
sudo chmod +x /etc/profile.d/path.sh
source /etc/profile.d/path.sh


#!/bash/sh
JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.265.b01-0.el8_2.x86_64
PATH=$PATH:$JAVA_HOME:$HOME/bin

export PATH

ln -s /opt/maven/apache-maven-3.6.3/bin/mvn /bin

#!/bash/sh
JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.265.b01-0.el8_2.x86_64
M2_HOME=/opt/maven/apache-maven-3.6.3
M2=$M2_HOME/bin
PATH=$PATH:$JAVA_HOME:$M2_HOME:$M2:$HOME/bin
export PATH


export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.265.b01-0.el8_2.x86_64
export M2_HOME=/opt/maven/apache-maven-3.6.3
export MAVEN_HOME=/opt/maven/apache-maven-3.6.3
export PATH=${M2_HOME}/bin:${PATH}

Maven setup

install package 


