#### Git常见操作命令
##### 更新已经在tracked的文件
```bash
git add -u
```

##### 添加文件更改包括tracked和没有tracked的文件
```bash
git add -A
```

##### 对一个文件内的修改有选择性添加到暂存区
```bash
git add -p
```

##### 给本次提交打tag
```bash
git tag v1
```

##### 导出从指定tag开始的历史提交逐一导出为patch文件
```bash
git format-patch v1..HEAD
```

##### 通过邮件发送补丁文件
```bash
git send-mail  *.patch
```

##### 修改最近的一次提交
```bash
git commit --amend
```

##### 修改历史提交
```bash
git rebase -i <commit-id>^
```

##### 移除错误包含的文件
```bash
git rm --cached <file>
```

#### Git分页器
git自带分页器，默认使用less -FRSX分页。

##### 分页器常见快捷键
- q ------------- 推出分页器
- h ------------- 显示分页器帮助
- 空格 --------- 下翻一页
- b ------------- 上翻一页
- d ------------- 下翻半页
- u ------------- 上翻半页
- j ------------- 上翻一行
- k ------------- 下翻一行
- /pattern ------ 向下寻找匹配内容[n(N)表示向前(后)继续寻找]
- ?/pattern ----- 向上寻找匹配内容[n(N)表示向前(后)继续寻找]
- g ------------- 跳到第一行[加数字跳到指定行]
- G ------------- 跳到最后一行[加数字跳到指定行]
- !<command> ---- 执行shell命令


##### 设置分页器自动换行
```bash
export LESS=FRX
```
或者
```bash
git config --global core.pager 'less -+$LESS -FRX'
```
