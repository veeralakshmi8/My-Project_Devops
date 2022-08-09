# Maven
# Introduction About Maven

It is a Build tool

It is used to jar(java based application), war(web based application), ear(interface application).

Depends on pom.xml---POM(Project Object Model),---XML(Extensible Markup Language)

POM contains all the data which is related to project. like dependencies, plugins etc

# Types of Build tools
Maven , Gradle, ANT

# Installation in AWS

In root

sudo yum install java-1.8.0-openjdk

cd /opt

wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz

untar the file

tar -xvf apache-maven-3.8.6-bin.tar.gz

Rename the tar file

mv apache-maven-3.8.6 maven

cd maven--cd conf---vi setting.xml---where all details available here we have to give the details of nexus or any artifactory details for storing the artifact

## we have to set up environment varible to work maven commands 

