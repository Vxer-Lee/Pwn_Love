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
<br/>
<br/>

## 基础知识
个人觉得Pwn的前置技能需要如下：
- 汇编基础
- GDB调试基础   
  以上基础可参考系列文章。
<br/>
<br/>


## 基础系列文章
## [《GDB调试基础》](./gdb_basic/readme.md)
<br/>

## PWN系列课程文章收集
## [《零基础入门PWN》](https://www.kanxue.com/book-57-853.htm)
## [《从0开始CTF-PWN》](https://bbs.pediy.com/thread-259272.htm)
## [《从入门到秃头之PWN蛇皮走位》](https://mp.weixin.qq.com/s/pEIKHPO-STNUM4VWE7pPng)
## [《CTF 竞赛入门指南PWN篇》](https://www.bookstack.cn/read/CTF-All-In-One/doc-3_topics.md)