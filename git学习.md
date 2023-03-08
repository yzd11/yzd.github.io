# Git基本理论（核心）

## 工作区域

1. 工作目录（Working Directory）
2. 暂存区(Stage/Index)
3. 资源区(Repository/Git Directory)
4. git仓库(Remote Directory)

![](C:\Users\17946\AppData\Roaming\Typora\typora-user-images\image-20230307200018812.png)

## 仓库搭建

### 本地仓库搭建



```git
# 在当前目录新建一个git 代码库
$ git init
```

### 远程仓库搭建

```
# 克隆一个项目和它的整个代码历史（版本信息）
$ git clone [url]
```

## GIT文件操作

![image-20230307202101454](C:\Users\17946\AppData\Roaming\Typora\typora-user-images\image-20230307202101454.png)

### 查看文件状态

``` 
#查看指定文件状态
git status [filename]

#查看所有文件状态
git status

# git add .                  添加所有文件到暂存区
# git commit -m "消息内容"    提交暂存区内容到本地仓库，-m 提交信息
# git checkout HEAD [filename] 从最后一次提交中的文件复制到工作区，进行恢复
# git remote add origin git@github.com:个人github名/仓库名.git
# git push -u origin master  将本地仓库push到GitHub上面。
-—添加后，远程库的名字就是origin，这是Git默认的叫法，也可以改成别的，但是origin这个名字一看就知道是远程库
```

