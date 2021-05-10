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
命令：git commit --all -m "这是一次性操作"