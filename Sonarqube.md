# Sonarqube

- code quality detect
- default port 9000

### Installation of sonarqube 

```
cd /opt
```
> install java
```
yum install java-1.8.0-openjdk unzip –y
```
> install sonarqube
```
https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-6.4.zip
```
> unzip file
```
unzip sonarqube-6.4.zip
```
> rename 
```
mv sonarqube-6.4 sonar
```
```
cd /sonar/bin/linux-x86-64
```
```
in that
sonar.sh is there --- used to start or stop the sonarqube
```
```
sh sonar.sh start
sh sonar.sh stop
sh sonar.sh status
```
```
cd /sonar/conf
vi sonar.properties 
```
```
- sonar.properties ---database related (mysql,oracle etc)data integrated here
- port number also can change here
```
```
default username and passwd- admin
```
## Integration of Sonarqube with Maven
- POM.xml 
```
<dependency>
<groupId>org.sonarsource.scanner.maven</groupId>
<artifactId>sonar-maven-plugin</artifactId>
<version>3.2</version>
</dependency>
```
```
<profiles>
<profile>
<id>sonar</id>
<activation>
<activeByDefault>true</activeByDefault>
</activation>
<properties>
<!-- Optional URL to server. Default value is http://localhost:9000 -->
<sonar.host.url>
http://192.168.2.174:9000
</sonar.host.url>
</properties>
</profile>
</profiles>
```
- Generate report
```
mvn sonar:sonar
```


