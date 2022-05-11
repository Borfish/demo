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

**工作区**：电脑中的目录就是工作区

**版本库**：版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支`master`，以及指向`master`的一个指针叫`HEAD`。![git-repo](https://www.liaoxuefeng.com/files/attachments/919020037470528/0)	     

​		git add的时候是吧文件修改添加到暂存区，git commit是提交到当前分支。同时，git跟踪的是修改，而非文件，如果修改过后没有add就不会commit到仓库中

​	`git checkout -- file`：把readme.txt文件在工作区的修改全部撤回

​	`git reset HEAD <file>`：把暂存区的修改撤销掉，重新放回工作区

​	`rm file`：删除工作区file文件	`git rm file`从版本库中删除文件	如果工作区删错了可以用`git checkout -- file` 恢复该文件

### 远程仓库



