git的使用方法

## 初始化.git仓库
- 创建一个新的.git文件
- 在当前目录下右键打开git bash
- 命令：git init

## 配置用户名及邮箱 
- 配置用户名：git config --global user.name "liuyang"
- 配置邮箱：git config --global user.email "liuyangestest@163.com"
- 这样每一次备份都会把备份者的信息进行存储

## 把代码存储到.git仓库中
- 把文件放在仓库门口：git add ./readme.md
- 把文件从门口放到仓库里：git commit -m "此处写说明"

## 查看状态
- 命令： git status
- 文件显示为红色代表没放在门口，只是改了代码
- 文件显示为绿色代表放在门口
- 文件出现nothing to commit即为全部保存了

## 放置多个文件
- 在这个文件夹里面的所有文件均放在仓库门口
- 命令：git add ./
- 接着使用commit把放在门口的变绿文件放进仓库里（commit不需要指定文件名）

## 一次性操作
- 直接将文件放到仓库里
- 命令：git commit --all -m "这是一次性操作"

## 查看修改日志
- 命令：git log
- 命令：git log --oneline
+ 把日志变成一行展示

## 回退到指定版本
- 命令：git reset --hard Head~0
+ 表示回退到上一次代码状态，就是最新的一次
- 命令：git reset --hard HEAD~1
+ 表示回退到上上次的代码状态
- 命令：git reflog
+ 表示展示对版本的切换记录显示
- 命令：git reset --hard [版本号]
+ 表示回退到指定版本号

## 分支
- 默认是有主分支master

## 创建分支
- 命令：git branch dev
+ 创建了一个dev分支
+ 在刚创建的dev分支里的东西和master主分支的东西一致

## 切换分支
- 命令：git checkout dev
+ 切换到指定分支，这里切换到dev
- 命令：git branch
+ 可以查看当前有多少分支

## 合并分支
- 命令：git merge dev
+ 合并当前分支，把当前分支与指定分支（dev）进行合并
+ 当前分支是指git branch命令中带*的分支
+ 把分支dev合并到master中来，需要先切回到master
- 合并时如果有冲突，需要手动去处理，处理后还要再提交一次

## github
- http://github.com
- 不是git，只是一个网站
- 这个网站允许通过git上传代码的功能

## 提交代码到github
- github当做git服务器来用
- 命令：git push https://github.com/Yleo-9/self_codes_backup.git master
+ 会把当前分支上传到云端的master上

## 把代码下载到本地
- 命令：git pull https://github.com/Yleo-9/self_codes_backup.git master
- 注意本地需要初始化一个仓储，即git init

## ssh方式上传代码
- 公钥 私钥
- 生成公钥和私钥
+ ssh-keygen -t rsa -c "liuyangestest@163.com"
