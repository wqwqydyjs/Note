## 安装配置java编译环境
### 1.安装java jdk（jdk1.8）
 
jdk路径上面不应该有中文字符，且安装完成后应该包含如下文件

![image](https://user-images.githubusercontent.com/55281287/128583968-85d70e92-cf8f-4cc9-b5ae-98b684d89189.png)

 
### 2.配置环境变量

a.用户变量:编辑path路径，新建两条路径
```
%JAVA_HOME%\bin
```
```
%JAVA_HOME%\jre\bin
```
b.系统变量

新建JAVA_HOME变量

变量名:
```
JAVA_HOME
```
变量值（按照上图中的路径）：
```
D:\coding\coding_tools\jdk1.8
```

新建/修改CLASSPATH变量
 
变量名：
```
CLASSPATH
```
变量值：
```
.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;
```







