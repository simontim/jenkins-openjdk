# Jenkins-openjdk
Installing a working instance debian based for implementing DevOps in totally open-sourced environments.



## Prerequisites
A Docker machine.
## Setting-up the container
  `docker pull openjdk:8-...`  
  `docker run -p ...`   
## Download and install Jenkins on Debian
  `cat distro`  
  `cd /etc/apt`  
  `echo ' ' >> source.list`  
  `apt-get install apt-transport-https`  
The reason of the following is explained in [1]  
`    export RUNLEVEL=1`  
`    apt-get install `  
## Start jenkins
Before starting take the inial Admin password:  
`    /root/.jenkins/secrets/`

# Appendix  

[1]: https://wiki.debian.org/it/RunLevel "Handle with RunLevel"  

[2]: https://wiki.jenkins.io/display/JENKINS/Starting+and+Accessing+Jenkins "Starting and Accessing Jenkins 060f9e60f94c498aab8a74a9e3a6c316"

[3]: https://stackoverflow.com/questions/9430559/background-process-in-linux "Start jenkins" 
