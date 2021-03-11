# Pwn_Love
Pwn入门学习笔记


## 环境搭建  
推荐Ubuntu 18.04及以上，个人用的是Deepin或Kali Linux  
```bash
sudo apt-get update  
sudo su  
sudo apt-get install python2.7 python-pip python-dev git libssl-dev libffi-dev build-essential  
sudo pip install --upgrade pip
sudo apt-get install git gdb gdb-multiarch
sudo apt-get install "binfmt*" 
git clone https://github.com/pwndbg/pwndbg
cd pwndbg
./setup.sh
sudo ./setup.sh
sudo pip install pwntools
sudo apt-get install qemu-user
sudo apt-get install gcc-multilib
```  
![avatar](.assets/1.png)  
![avatar](.assets/2.png)
<br/>
<br/>
Mac系统上我用的是docker  
https://hub.docker.com/r/skysider/pwndocker  
```
docker run -d \
    --rm \
    -h ${ctf_name} \
    --name ${ctf_name} \
    -v $(pwd)/${ctf_name}:/ctf/work \
    -p 23946:23946 \
    --cap-add=SYS_PTRACE \
    skysider/pwndocker

docker exec -it ${ctf_name} /bin/bash
```
