# Jenkins-openjdk
How to install a Jenkins Server Debian based.
## Prerequisites
A Docker machine with the port 8080 available.
## Setting-up the container
`docker pull openjdk:8-jdk`  
`docker run -it -p 8080:8080 openjdk:8-jdk bash`   
## Download and install Jenkins on Debian
With the root user: 
`cat /etc/os-release`  
`wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | apt-key add -`  
`cd /etc/apt`  
`echo 'deb https://pkg.jenkins.io/debian-stable binary/' >> sources.list`  
`apt-get install apt-transport-https`  
`apt-get update`  
The reason of the following is explained in [1]  
`export RUNLEVEL=1`  
`apt-get update`  
`apt-get upgrade`  
`apt-get install jenkins`  
## Start jenkins  
Before starting take the inial Admin password:  
`/root/.jenkins/secrets/`  
`cat initialAdminPassword`   
Now start the application in background:  
`cd /usr/share/jenkins`  
`java -jar jenkins.war > /log.txt &`  
`disown`  
`exit`  

And see the browser at http://yourhost:8080 

[1]: https://wiki.debian.org/it/RunLevel "Handle with RunLevel"  

[2]: https://wiki.jenkins.io/display/JENKINS/Starting+and+Accessing+Jenkins "Starting and Accessing Jenkins 060f9e60f94c498aab8a74a9e3a6c316"

[3]: https://stackoverflow.com/questions/9430559/background-process-in-linux "Start jenkins" 
