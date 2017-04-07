# 条件：ubuntu默认安装 
安装路径：`/usr/bin/`

需要自己在`/usr`路径下创建一个data文件夹，进入data文件夹创建一个db文件夹
![](https://raw.githubusercontent.com/jiangyoubushiyou/learn_note/master/img/mongo.png)
## mongodb启动
要cd到安装路径`/usr/bin`下运行命令

```
sudo mongod --dbpath=/usr/data
```

ps:无法运行可以尝试重启

```
sudo reboot
```

输入密码重启

# 用ubuntu shell启动mongodb
## 第一步 编写shell脚本
新建一个文件，扩展名为sh

用vim打开文件编写

输入代码，第一行一般是
     
    #!/bin/bash 


    cd /usr/bin

    sudo mongod --dbpath=/usr/data



"#!"是一个约定的标记，它告诉系统这个脚本需要什么解释器来执行

## 第二步 运行
运行shell脚本有两种方法：
### 1.作为可执行程序

    chmod +x start_mongodb.sh
    ./start_mongodb.sh
注意，一定要写成./start_mongodb.sh，而不是start_mongodb.sh，用./start_mongodb.sh告诉系统说，就在当前目录找。

通过这种方式运行bash脚本，第一行一定要写对，让系统可以查找到正确的解释器。
### 2.作为解释器参数
这种运行方式是直接运行解释器，其参数就是shell脚本的文件名，

    /bin/sh start_mongodb.sh

这种方式运行的脚本，不需要在第一行指定解释器信息，写了也没用。
