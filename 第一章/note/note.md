#### diff和patch工具
- diff用于比较两个文本的差异
- patch可以根据差异文件恢复出原文件

注意：diff和patch工具不支持二进制文件的差异比较。

##### diff命令
```bash
diff -Naur code1.txt code2.txt > diff.txt
```
**-u** 参数用于在差异输出时可以带上下文。

##### patch命令
```bash
patch -R code2.txt < diff.txt
```
