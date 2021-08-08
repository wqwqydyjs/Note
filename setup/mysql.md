## mysql安装配置及navicat的安装
### 1.下载mysql
在安装mysql前需要安装visual studio。

[mysql下载地址](https://dev.mysql.com/)；

下载mis版本的安装程序，（虽然只标明了32位的，但是32位的mis安装程序里面有64位的，所以直接下载64位的即可）按照提示一步步安装即可


### 2.配置mysql环境变量
找到mysql server目录下面的bin文件夹路径，如下图所示


![image](https://user-images.githubusercontent.com/55281287/128621566-cbf64a79-caf2-4131-babc-71f23a19b15d.png)
 
在环境变量的path变量中编辑添加上bin文件夹的路径即可
 
![image](https://user-images.githubusercontent.com/55281287/128621588-6ece82e8-8317-43c6-b17b-71bf058e760c.png)
![image](https://user-images.githubusercontent.com/55281287/128621600-c0d356c7-653c-4521-8187-a152a7f2d6be.png)
 
### 3.检测是否安装成功
启动mysql：将命令行切换到mysql的bin目录下面输入
```
 net stat mysql 
 ```
 登录mysql(密码是在安装mysql过程中设置的，能成功登录说明安装成功): 
 ```
 mysql -u root -p
 ```
 ### 4.Navicat安装及破解教程
 [完整安装及破解教程](https://www.jb51.net/article/199496.htm)




