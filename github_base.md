# github的基本使用以及注意事项
## 1.安装git bash
  Windows直接下载git bash，双击进行安装，安装目录可以自行修改一下，其他一些选项全都默认即可[下载地址](https://gitforwindows.org/)
## 2. ssh公钥配置
  ### 2.1生成秘钥对
  打开git bash，直接使用以下命令生成，如有选择提示直接回车使用默认值即可：
  ```
  ssh-keygen -t rsa -P 
  ```
  结果如下
  
  ![image](https://user-images.githubusercontent.com/55281287/126855665-e0fed9e9-5bd4-4231-9c93-520fb99e7db9.png)
  
  生成的秘钥对如下所示，其中公钥是一行没有换行的字符。
  
  ![image](https://user-images.githubusercontent.com/55281287/126855704-b2ca8b31-eafd-426c-a27d-db449ec7bb91.png)
  
  ### 2.2把ssh公钥导入到github上面
  github左上角用户处点击展开，点击Settings。
  
  切换到“SSH and GPG keys”，点击“New SSH key”
  
  ![image](https://user-images.githubusercontent.com/55281287/126856118-a4e61a05-e38b-451e-bb4e-df030af913a6.png)
  
  ### 2.3配置提交代码时登记的邮箱和用户
  这个邮箱和用户只是为了方便回溯代码是谁提交的，并不需要是github的邮箱和用户名，甚至是可以随便写的邮箱和用户名
  
  ![image](https://user-images.githubusercontent.com/55281287/126856188-7829e418-0e24-4ca9-a929-939b87ee1b2e.png)
## 3.在github托管代码
用git bash直接创建git托管项目

用git clone +“ssh地址”克隆远程仓库

在各种编辑器里面可以直接进行pull push等管理操作

常见git命令如下

```
git --help //帮助,可以查看git 的各种方法操作

git init //创建一个新的仓库，在当前目录下或生成一个 .git 的子目录， 让当前目录变成git可管理的仓库， 以后所有的文件变化信息都会保存在这个文件下。.git 文件中有一个config文件 可以更改配置。

git status //查看状态，可以知道那些文件发生了变化，那些文件还没有提交到仓库中去等。建议在提交前查看状态，以确认发生变化的文件已经添加至缓存中。

git add * / . //添加当前目录下的多有文件和子目录到缓存中
git add filename //添加指定文件到缓存中，多个文件一起添加时中间用空格隔开
git add f* //提交所有以f开头的文件

git commit -m "注释内容" //提交缓存至仓库中，每一次提交git就会为全局代码提供一个commit唯一标识（版本号，就是在产看日志时 最前面的那一串字符串），用户可以通过git reset 回溯到任意一次提交的位置。

git log //查看提交日志 包括每次的版本变化，版本变化对应的commit标识也会改变
git log --pretty=oneline //提交体质的简介显示方案
git reflog //获取版本号
git log --graph //以树形结构查看分枝状态，提交日志

git reset --hard HEAD^^ //回溯到上一次提交
git reset --hard 版本号 //回溯到指定版本

git diff filename //查看更改前后的区别

git branch //查看分支 git默认有一个主分支master，当多分之时，分支前有*的单表当前所在分支
git branch branchname //创建分支，branchname为分支名
git branch -b branchname //创建一个分支，并切换到此分支
git branch -d branchname //删除分支 注意要在分支所在的主干上进行删除
git checkout branchname //切换到指定分支
git checkout - //快速切换到上一个分支
git merge //合并分支

//将本地库推送至github上，首先要在github创建一个项目
git remote add origin git@github.com:uesr.name/project.name.git // user.name代表github的用户名，project.name代表在github上创建的项目名称。此步骤为了把本地仓库和远程仓库关联起来，用来首次推送，以后在进行推送时则不需要执行此步骤
git push -u -origin master //首次推送时输入完整结构，之后的推送输入git push即可
git pull origin master //从远程仓库中拉下新的改动

git clone url // github仓库中的项目克隆到本地， url即为github中克隆的地址
```


 
 



  
  
  
