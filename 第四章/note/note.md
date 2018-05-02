#### Git初始配置
- 配置全局用户名和邮箱
```bash
git config --global user.name "codekongs"
git config --global user.email "szh@codekong.cn"
```

- 清空用户名和邮箱配置
```bash
git config --unset --global user.name
git config --unset --global user.email
```

- 配置项目用户名和邮箱
```bash
git config user.name "codekongs"
git config user.email "szh@codekong.cn"
```

- 为系统所有用户配置Git命令别名
```bash
sudo git config --system alias.ci commit
```

- 为本用户配置Git命令别名
```bash
git config --global alias.ci commit
```

- 在Git命令输出中开启颜色显示
```bash
git config --global color.ui true
```


#### Git目录相关
- 显示版本库.git目录所在位置
```bash
git rev-parse --git-dir
```

- 显示工作区根目录
```bash
git rev-parse --show-toplevel
```

- 相对于工作区根目录的相对目录
```bash
git rev-parse --show-prefix
```

- 从当前目录后退到工作区的根的深度
```bash
git rev-parse --show-cdup
```


#### Git配置文件

- Git涉及到三个配置文件
 - 项目配置文件[workspace/.git/config]
 - 用户配置文件[~/.gitconfig]
 - 系统配置文件[/etc/gitconfig]

> 上面的三个文件的优先级依次降低。


- Git查看修改配置文件

```bash
git config -e

git config -e --global

git config -e --system
```

> Git配置文件采用INI文件格式，可以通过命令读取和修改。

##### 修改提交的用户信息
可以对已经提交的用户的信息进行修改，修改的过程是进行一次空白提交。
先要通过命令设置正确的用户名和邮箱。
```bash
git commit --amend --allow-empty --reset-author
```
- --amend是修补上一次的提交来修改用户名和邮箱，不产生新的提交
- --allow-empty是允许进行空白提交
- --reset-author是重置修改提交者的ID
