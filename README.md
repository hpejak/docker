# Docker


## Install Docker
##### Official installer script

<sup>

[Script Link](https://get.docker.com/)

</sup>

##### Centos Personal Check
<sup>

- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-cli-19.03.9-3.el7.x86_64.rpm  
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.3.7-3.1.el7.x86_64.rpm  
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-19.03.9-3.el7.x86_64.rpm  
 
- sudo yum install docker-ce-cli-19.03.9-3.el7.x86_64.rpm  
- sudo yum install containerd.io-1.3.7-3.1.el7.x86_64.rpm  
- sudo yum install docker-ce-19.03.9-3.el7.x86_64.rpm


systemctl start docker

</sup>

## Install docker-compose
##### Linux 

<sup>

curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose

</sup>

## Docker Image Export Import

<sup>

- docker pull hello-world  
- docker save --output hello-world.tar {your image name or ID}  
- $docker load --input hello-world.tar  

</sup>

## Start Docker on system startup
<sup>

sudo systemctl enable /usr/lib/systemd/system/docker.service

</sup>