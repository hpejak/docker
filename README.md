# Docker


## Install Docker
##### Official installer script

<sup>

[Script Link](https://get.docker.com/)

</sup>

##### Centos Personal Check
<sup>
 
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-scan-plugin-0.8.0-3.el7.x86_64.rpm
 
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-cli-19.03.9-3.el7.x86_64.rpm [OLD]
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-cli-20.10.8-3.el7.x86_64.rpm
 
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.3.7-3.1.el7.x86_64.rpm [OLD] [DEPRECATED]
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.4.9-3.1.el7.x86_64.rpm
 
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-rootless-extras-20.10.8-3.el7.x86_64.rpm
 
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-19.03.9-3.el7.x86_64.rpm [OLD]
- sudo wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-20.10.8-3.el7.x86_64.rpm
 
 
 
- sudo yum install docker-ce-cli-19.03.9-3.el7.x86_64.rpm [OLD] [DEPRECATED]
- sudo yum install containerd.io-1.3.7-3.1.el7.x86_64.rpm [OLD] [DEPRECATED]
- sudo yum install docker-ce-19.03.9-3.el7.x86_64.rpm [OLD] [DEPRECATED]

- sudo yum install docker-ce-cli-19.03.9-3.el7.x86_64.rpm
- sudo yum install docker-scan-plugin-0.8.0-3.el7.x86_64.rpm
- sudo yum install docker-ce-cli-20.10.8-3.el7.x86_64.rpm
- sudo yum install containerd.io-1.4.9-3.1.el7.x86_64.rpm
- sudo yum install docker-ce-19.03.9-3.el7.x86_64.rpm
- sudo yum install docker-ce-rootless-extras-20.10.8-3.el7.x86_64.rpm
- sudo yum install docker-ce-20.10.8-3.el7.x86_64.rpm

systemctl start docker

</sup>

##### Ubuntu Personal Check
<sup>
 
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/docker-ce-cli_20.10.5~3-0~ubuntu-bionic_amd64.deb [OLD] [DEPRECATED]
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/docker-ce-cli_20.10.8~3-0~ubuntu-bionic_amd64.deb
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/containerd.io_1.4.4-1_amd64.deb [OLD] [DEPRECATED]
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/containerd.io_1.4.9-1_amd64.deb
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/docker-ce_20.10.5~3-0~ubuntu-bionic_amd64.deb [OLD] [DEPRECATED]
- sudo wget https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/docker-ce_20.10.8~3-0~ubuntu-bionic_amd64.deb

- sudo dpkg -i docker-ce-cli_20.10.5~3-0~ubuntu-bionic_amd64.deb [OLD] [DEPRECATED]
- sudo dpkg -i containerd.io_1.4.4-1_amd64.deb [OLD] [DEPRECATED]
- sudo dpkg -i docker-ce_20.10.5~3-0~ubuntu-bionic_amd64.deb [OLD] [DEPRECATED]
 
- sudo dpkg -i docker-ce-cli_20.10.8~3-0~ubuntu-bionic_amd64.deb
- sudo dpkg -i containerd.io_1.4.9-1_amd64.deb
- sudo dpkg -i docker-ce_20.10.8~3-0~ubuntu-bionic_amd64.deb
</sup>

##### Manage Docker as a non-root
sudo usermod -aG docker $USER
newgrep docker

## Install docker-compose
##### Linux 

<sup>

curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
 
curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
 
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
