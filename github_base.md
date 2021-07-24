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


 
 



  
  
  
