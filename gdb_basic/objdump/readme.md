# objdump使用详细教程
> https://ivanzz1001.github.io/records/post/linux/2018/04/09/linux-objdump    
> https://man.linuxde.net/objdump

## 常用命令
```bash
#用来显示文件头
objdump -f xxx
#用来显示段信息
objdump -h xxx
#十六进制显示text段信息
objdump -s -j .text xxx
#显示符号表
objdump -t xxx
#只显示text段的符号表
objdump -j .text -t xxx
#显示text段的反汇编内容
objdump -j .text -d xxx
#Intel x86格式显示
objdump -j .text -M intel -d xxx
#不显示字节码的反汇编显示
objdump -j .text -M intel --no-show-raw-insn -d xxx
#显示某函数的反汇编显示
objdump -j .text -M intel --no-show-raw-insi -d xxx | awk -v RS= '/^[[:xdigit:]].*<test>/'
#根据开始地址，结束地址来显示反汇编内容
objdump -M intel --no-show-raw-insn -d xxx --start-address=0x00411735 --stop-address=0x0041a880
```