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

