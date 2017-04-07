# 条件：ubuntu默认安装 
安装路径：`/usr/bin/`

需要自己在`/usr`路径下创建一个data文件夹，进入data文件夹创建一个db文件夹
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