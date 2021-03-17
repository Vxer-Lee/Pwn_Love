# radare2 学习笔记

## [radare2中文版Wiki](http://fucklee.gitbook.io/radare2)

还是记录下我最近用的吧：
```bash
#加载程序，然后分析
r2 pwnme
aaa
#列出他的符号表，或者说是函数
afl #function list
s sym.bot13 #跳转到bot13函数这个地址
pdf #以汇编显示显示bot13函数
vv #tui格式显示
VV #流程图的格式，类似IDA的空格功能.
```