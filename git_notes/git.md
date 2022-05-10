# git仓库教程

发明初衷：代码版本管理。分布式版本控制。

### 基本操作

git init ：建库				git status：查看当前藏库状态				gti diff：查看尚未提交的内容和原版的区别	

git log：查询版本迭代的历史记录（参数 --pretty=oneline可以简化输出）前面的长串16进制数未版本号	

HEAD当前版本	HEAD^上个版本	HEAD~x:上x个版本	

git reset --hard HEAD^：回到上一个版本

下图为版本更新原理，如果从过去版本恢复到现在版本需要知道版本号，可以用git reflog（记录每一次命令）来查询版本号

![image-20220511024535916](C:\Users\borfish\AppData\Roaming\Typora\typora-user-images\image-20220511024535916.png)	

### 基本概念

