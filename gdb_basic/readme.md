# GDB调试基础  

## [objdump详细使用教程](/objdump/readme.md)  
## [readelf详细使用教程](/readelf/readme.md)  
## [radare2学习笔记](/radre2/readme.md)  
<br>
<br>

## 前言
GDB（GNU Debugger）是UNIX及UNIX-like下的强大调试工具，可以调试ada, c, c++, asm, minimal, d, fortran, objective-c, go, java,pascal等语言。本文以C程序为例，介绍GDB启动调试的多种方式。
<br/>
<br/>

## 查看文件头信息
### #readelf （个人喜欢）
```
readelf -h pwnme
```
### #objdump
```
objdump -f pwnme
```
![avatar](.assets\1.png)  

<br/>
<br/>

## 查看段信息

### #readelf（个人喜欢）
```
readelf -S pwnme
```
![avatar](.assets\2.png)  
### #objdump
```
objdump -h pwnme
```
![avatar](.assets\3.png)  
### #Detect-It-Easy
![avatar](.assets\4.png)  
<br/>
<br/>

## 查看符号表

### #readelf
```
readelf -s pwnme
```
![avatar](.assets\5.png)  
### #objdump
```
objdump -t pwnme
```
![avatar](.assets\5.png)  

### radare2（个人喜欢）
```
r2 pwnme
aaa
afl
```
![avatar](.assets\6.png)  

> https://www.yanbinghu.com/2019/04/20/41283.html
> https://linuxtools-rst.readthedocs.io/zh_CN/latest/tool/gdb.html
> https://chujian521.github.io/blog/2020/03/01/GDB%E9%80%86%E5%90%91%E8%B0%83%E8%AF%95%E5%88%86%E6%9E%90/
> https://wiki.ubuntu.org.cn/%E7%94%A8GDB%E8%B0%83%E8%AF%95%E7%A8%8B%E5%BA%8F
