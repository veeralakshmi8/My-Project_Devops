
# Nexus
### Introduction of Nexus
- open source
- Artifactary Tool
- To store Artifact
- Default port number 8081

### Types of Artifactory Tools
- Nexus
- Jfrog

### Installation of Nexus
- Install java
```
sudo yum install java-1.8.0-openjdk.x86_64 -y
```

```
cd /opt
```
- Install nexus
```
sudo wget -O nexus.tar.gz https://download.sonatype.com/nexus/3/latest-unix.tar.gz
```
- Extract the file
```
tar -xvf nexus.tar.gz
```
- Rename
```
mv nexus.tar.gz nexus
```
```
sonatype-work has passwords
```
- Need to change the username of the nexus
```
useradd nexus
```
```
chown -R nexus:nexus nexus
```
```
cd /nexus/bin
1.nexus has stript to start or stop the nexus
 sh nexus start
2.nexus.rc --mentions about the user where it has to run 
3.nexus.vmoption--min and max memory has to integrate
```

