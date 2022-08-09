# Maven
### Introduction About Maven

- It is a Build tool

- It is used to jar(java based application), war(web based application), ear(interface application).

- Depends on pom.xml---POM(Project Object Model),---XML(Extensible Markup Language)

- POM contains all the data which is related to project. like dependencies, plugins etc

- Mandatary in POM.xml options---Project, modelVesion, Groupid, artifactId,version

### Types of Build tools
- Maven , Gradle, ANT

### Installation in AWS

#### In root

- Install java
```
sudo yum install java-1.8.0-openjdk
```
- Install maven--any software best practice to install in /opt
```
cd /opt

wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
```
- untar the file
```
tar -xvf apache-maven-3.8.6-bin.tar.gz
```
- Rename the tar file
```
mv apache-maven-3.8.6 maven
```
- cd maven--cd conf---vi setting.xml---where all details available here we have to give the details of nexus or any artifactory details for storing the artifact

##### we have to set up environment varible to work maven commands 

```
cd /etc/profile.d/
```
- vim maven.sh 
- change permissions(chmod 777 maven.sh)

```
# Apache Maven Environment Variables

# MAVEN_HOME for Maven 1 - M2_HOME for Maven 2

export M2_HOME=/opt/maven

export PATH=${M2_HOME}/bin:${PATH}
```
- source maven.sh

## creation of java file in maven 

- mvn archetype:generate

- refer repo.apache.maven.org--contains all plugins

- groupid means company reverse order has to give like com.tcs---package also same

- artifactid means project name


#### Build Life Cycles

Validate-Complile(convert java to .class files)-Test-Package(generate jar or war)-Verify-Install-Deploy

### Commands
 mvn validate
 
 mvn compile
 
 mvn test etc...
