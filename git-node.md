1. git简介
- git是一个分支管理系统，可以将其理解为代码的仓库，其作用是可以在开发项目的过程中创建多个分支，每个分支都可以对应一个开发人员，在项目准备上线的时候可以将多个分支进行合并，适用于团队开发，同时还可以存储项目的不同版本，便于回退以及维护项目
- git使用前需要安装，安装完成后在命令行输入 git -v，正常显示版本后代表安装成功

2. git的配置
 - git在使用前需要先配置一下name和email，用于区分不同的用户(开发人员)	

```
git config --global user.name "xxx"	
git config --global user.name "xxx@xxx.com"
```
3. git的状态
 - 未跟踪：文件未被git管理
 - 已跟踪：文件已被git管理
 - 已跟踪有如下几种状态：
 ```
- 暂存：表示文件修改已经保存，但是未被提交到git仓库中
- 未修改：git仓库中的文件和当前已跟踪的文件一样
- 已修改：文件发生了变化，和git仓库中记录的文件不一样
 ```

4. git的使用
```
git init 用于初始化项目，初始化以后在初始化的目录下会出现一个.git目录(隐藏目录)
git add <filename> 将未跟踪状态的文件设置为暂存状态，* 代表当前目录下的所有文件
git commit -m 提交文件到git仓库中(不包括未跟踪)，文件由暂存状态变为未修改状态，m代表描述信息
git commit -a -m 提交所有已修改的文件(不包括未跟踪)
git log 查看git的操作日志,按q退出
```
- git的回退：
```
git restore <filename> 将指定文件回退到git仓库中最新的状态
git restore --staged <filename> 取消暂存状态
```
- git的删除：
```
git rm <filename> 将指定的文件删除(暂存状态)
git rm <filename> 强制删除
```
- 文件的移动(重命名)
```
git mv <filename> <filename> 重命名
```