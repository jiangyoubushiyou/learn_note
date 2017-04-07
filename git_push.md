# 本地项目文件夹已经存在，git上传
## 第一步：创建远端仓库
登录**github**，新建一个仓库，**“New repository”**，可以得到仓库的https地址**example：https://github.com/jiangyoubushiyou/example.git**
![](https://github.com/jiangyoubushiyou/learn_note/img/step1.png)
## 第二步 建立本地git仓库
在本地项目文件夹的目录下，执行git命令

```git init ```
## 第三步 将本地项目的所有文件添加到仓库中
```
git add .
```

如果想添加某个特定的文件，把.换成特定的文件名；
## 第四步 将add的文件commit到仓库
```
git commit -m "注释语句"
```
## 第五步 将本地的仓库关联到github上
```
git remote add origin https://github.com/jiangyoubushiyou/example.git
```

http连接换成自己创建的仓库url地址，https://github.com/github用户名/仓库名.git

##第六步 上传代码到github远程仓库
```
git push origin master
```

之后可能会让输入username和password，只要输入github账号密码就可以了，执行完后没有异常就表示上传成功，可以在github上刷新查看。
