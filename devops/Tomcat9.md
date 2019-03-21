# Documentation serveur Apache Tomcat 9

## Installation and execution

- First, download the last version of Tomcat (or the one you need) [here](https://tomcat.apache.org/download-90.cgi). Download the Core version.
- Once you downloaded the installation, unpack the binary distribution into a convenient location. For example, in **C:\apache-tomcat-x.x.xx** on Windows, or **/usr/local/apache-tomcat-x.x.xx** on Linux/Unix and create **CATALINA_HOME** environment variable pointing to these locations

Tomcat can be started by executing the following commands :
(Windows)
```
%CATALINA_HOME%\bin\startup.bat
<path-to-tomcat>\bin\startup.bat
```

(Linux/Unix)
```
$CATALINA_HOME/bin/startup.sh
/path/to/tomcat/bin/startup.sh
```
After a successful startup, the default web-applications included with Tomcat will be available by visiting http://localhost:8080/.

## Links and sources

Lien vers un tuto expliquant le principe d'une Web app, du protocole HTTP et détaillant le procédé d'installation d'un serveur Apache Tomcat 9 :
https://www.ntu.edu.sg/home/ehchua/programming/howto/Tomcat_HowTo.html
