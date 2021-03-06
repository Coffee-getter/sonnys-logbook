
<b>背景需求</b>

很多时候我们都是在gitlab上拉取现有的项目下来做开发。但是假设一个新项目由你来搭建项目框架，你本地新建项目，也搭好了初始化的项目框架。
现在需要把这个项目放到公司gitlab仓库中，方便其他同学拉取该项目做后续的具体开发，具体应该如何做呢？

<b>具体步骤</b>

一、gitlab上新建一个空白项目 <br/>
gitlab上点击new project按钮，新建一个项目<br/>
点击 create project 按钮创建出该空白的项目<br/>

![image](https://user-images.githubusercontent.com/70362312/168512363-fb0a82a0-e62f-4c12-94fd-2f655eb32db2.png)



二、初始化本地仓库并commit项目<br/>
进入本地该项目目录下，右键Git Bash Here打开git命令窗口：<br/>

![image](https://user-images.githubusercontent.com/70362312/168512456-bb843d35-38bf-4716-8858-0ff36150f568.png)


```
git init 
git add .
git commit -m "初始化项目"

初始化本地仓库
提交代码到暂存区
commit提交项目
```


三、建立连接并推送

```
git remote rm origin
git remote -v
git pull --rebase origin master
git remote add origin  https://gitlab.xx.com/xxxx.git
git push -u origin master

前三步为确保无连接的步骤
1.移除原有连接的远程
2. 查看有没有连接的远程
3. 拉取远程的代码，以防提交的时候发生错误
然后，尝试建立本地仓库和远端gitlab仓库关系
最后，push本地代码到远程
```

