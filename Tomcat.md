# Tomcat
### Introduction
- Tomcat is a application server.
- open source
- Used to deploy war file.
- Default port 8080 (we can change).

## Install Tomcat in centos 7

```
cd /opt
```

> install java
```
sudo yum install java-1.8.0-openjdk
```


> install tomcat

```
https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.106/bin/apache-tomcat-7.0.106.tar.gz
```
> untar tar file
```
tar -xvf apache-tomcat-7.0.106.tar.gz
```
> rename the file as tomcat
```
mv apache-tomcat-7.0.106 tomcat
```
- Go to tomcat
```
cd tomcat
cd bin
```
sh startup.sh
```

- startup.sh-- to start the service
- shutdown.sh--to stop the service
- to start or stop the service catalina.sh should have execute permission
- startup.bat, shutdown.bat -- for windows
```

```
cd conf
- vi server.xml--tomcat default port number will be there we can change.--- if two tomcat servers are there server ports should be different for both.
```
```
vi tomcat-users.xml
```
- tomcat-users.xml- contains credencials
```
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>   
<role rolename="admin-gui"/>
<role rolename="admin-script"/>

<user username="tomcat" password="tomcat" roles="manager-gui, admin-gui, manager-status,manager-script,manager-jmx,admin-script"/>

```

```
cd webapps
```
- webapps contains default applications
- if we want to deploy new application we have to deploy here
```
cd log
```
- catalina.out-- see the logs 
