tomact ::
ln -s /opt/apache-tomcat-8.5.58/bin/startup.sh /bin/tomcatup
  ln -s /opt/apache-tomcat-8.5.58/bin/shutdown.sh /bin/tomcatdown
  tomcatup

unlink /bin/tomcatup



find / -name context.xml


<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>
<user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
<user username="deployer" password="deployer" roles="manager-script"/>
<user username="tomcat" password="s3cret" roles="manager-gui"/>


clean install package 


curl https://awscli.amazonaws.com/awscli-exe-linux-x86_64-2.0.30.zip  -o awscli-bundle1.zip

 unzip awscli-bundle1.zip
 
 ./awscli-bundle1/install -i /usr/local/aws -b /usr/local/bin/aws