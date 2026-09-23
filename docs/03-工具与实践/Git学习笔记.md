# Git回顾帮助文档
* * *
*此文档为学习Git时所写,仅作为学习辅助工具分享交流, 无权威性

made by ***zkerur***  
from up主 ***狂神说***
* * *
![Git](https://git-scm.com/images/logo@2x.png)
* * *
## Git中可能用到的Linux的基础命令

```bash
cd    #改变目录
cd..  #回退到上一个目录,直接cd进入默认目录
pwd   #显示当前目录所在路径
ls/ll
touch
rm    #删除文件
mkdir #新建一个文件夹,rm -r src 删除src目录
mv    #移动文件到指定的目录,mv 文件名 指定的目录
reset #重新加载终端
clear
history
help
exit
```
* * *
## 一些基础性配置
### [下载Git](https://git-scm.com/)并安装Git

*无需特殊配置, 自动配置环境变量*

* 使用git config --global --list查看配置情况
* 使用git config --global user.name "用户名"配置用户名
* 使用git config --global user.email "邮箱名称"配置邮箱名称
* * *
## Git基本理论
### 工作区域
* 工作目录 Working Directory
* 暂存区 Stage/Index
* 资源库 Repository/Git Directory
* 远程git仓库 Remote Directory

### 文件状态
* Untracked 未跟踪  
* Unmodify 文件已入库未修改  
* Modified 文件仅修改  
* Staged 暂存  
(^/ω＼^)ノ
* * *
## 项目搭建
### 第一步 创建本地仓库
#### 方案一 初始化
选择一个文件夹右键使用 `git bash here`  
执行 `git init` 生成一个隐藏的.git文件
#### 方案二 使用克隆
选择一个文件夹右键使用 `git bash here`  
执行 `git clone {url地址}`将远程仓库的内容克隆到本地
### 第二步 GIT文件操作
执行`touch 文件名`创建一个新的文件  
执行`git status`显示该文件untracked  
执行`git add .`以将文件添加到暂存区  
执行`git commit -m "new file 文件名"`提交暂存区到本地仓库  
#### 忽略文件

**基础语法规则**

* 空行：不匹配任何文件，可用于分组，提高可读性。  
* 注释：以 # 开头，用于说明。  
* 精确匹配：直接写文件名，如secret.txt只忽略根目录下的这个文件。  
* 目录匹配：以 / 结尾，如 build/，
忽略所有名为 build 的目录。开头加 / 表示根目录，
如 /TODO 只忽略根目录的 TODO 文件。

**通配符**

* *：匹配0个或多个字符（不含路径分隔符 /），如 *.log 忽略所有日志文件。
* **：匹配任意层级目录，如 **/temp 
忽略所有层级的temp文件夹，logs/**/*.log 
忽略 logs 目录下任意深度的日志文件。
* ?：匹配任意一个字符。
* 否定规则：用 ! 取反。常用于排除整个目录后，
再包含其中的特定文件。例如：

```text
build/          # 忽略build目录
!build/index.js # 但追踪 build/index.js 文件
```
> 注意 .env、node_modules/、dist/ 这三大金刚必加，
> 其他规则按需补充；如果文件已追踪，记得先 git rm 
> --cached 再提交。这样仓库就能始终保持干净、
> 安全、可移植。
* * *
## 实践
访问[GitHub](https://github.com/) 访问[Gitee](https://gitee.com/)
1. 注册Git平台账号完善个人信息
2. 设置本机绑定SSH公钥, 实现免密码登录  
   进入用户文件夹下的 .ssh 目录  
   生成公钥  
   在当前文件夹右键使用 `git bash here`  
   执行`ssh-keygen -t {加密算法(官方推荐rsa)}`
3. 以rsa加密算法为例, 将生成的公钥id_rsa.pub打开,   
   将里面的内容复制并黏贴到Git平台账号中的对应位置即可  
4. 使用Git平台创建一个自己的仓库
5. 克隆到本地  
   执行 `git clone {url地址}`将远程仓库的内容克隆到本地
* * *
## 通过IntelliJ IDEA





