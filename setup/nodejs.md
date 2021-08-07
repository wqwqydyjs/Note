## nodejs安装配置
### 下载nodejs
[nodejs下载及源码地址](https://nodejs.org/en/download/)
### 配置nodejs的环境变量
#### 1.创建文件夹保存缓存及全局安装文件
说明：环境配置主要配置的是npm安装的全局模块所在的路径，以及缓存cache的路径，之所以要配置，是因为以后在执行类似：npm install express [-g] （后面的可选参数-g，g代表global全局安装的意思）的安装语句时，会将安装的模块安装到【C:\Users\用户名\AppData\Roaming\npm】路径中，占C盘空间。
例如：我希望将全模块所在路径和缓存路径放在我node.js安装的文件夹中，则在我安装的文件夹【D:\coding\coding_tools\nodejs】下创建两个文件夹【node_global】及【node_cache】如下图：
![image](https://user-images.githubusercontent.com/55281287/128585183-efe67c38-8908-4da6-9912-eb235a2a1c9d.png)

文件夹创建完成后命令行输入：
```
npm config set prefix "D:\coding\coding_tools\nodejs\node_global"
```
```
npm config set cache "D:\coding\coding_tools\nodejs\node_cache"
```

如下图所示：

![image](https://user-images.githubusercontent.com/55281287/128585270-be9805dc-1844-4394-a672-04116231ff71.png)
#### 2.配置环境变量
##### a.系统变量
新建变量

变量名：```NODE_PATH```

变量路径：```D:\coding\coding_tools\nodejs\node_global\node_modules```

##### b.用户变量
编辑path变量，增加路径
```
D:\coding\coding_tools\nodejs\node_global
```
#### 3.测试是否配置成功
安装个module进行测试
```
npm install express -g     # -g是全局安装的意思
```
成功的结果如下所示：
![image](https://user-images.githubusercontent.com/55281287/128585465-7493cd51-344c-49fb-9258-2f1d86fe5dc6.png)
#### 4.安装镜像用cnpm来代替npm 进行下载加快速度（使用淘宝镜像）
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
