# Git 常用命令

## 基本仓库命令
- 创建版本库： 进入目录，执行 git init
- 添加远程仓库：git remote origin 远程仓库地址
- 从远程仓库克隆：git clone 远程仓库地址
- 查看文件的状态 git status
- 查看修改的内容：git diff tgb.txt
- 查看历史版本：　git log

## git 分支

- 查看分支：git branch 【name】
- 创建分支：git branch  【name】
- 切换分支:git checkout 【name】
- 创建+切换分支：git checkout -b 【name】
- 合并某分支到当前分支：git merge 【name】
- 删除分支：git branch -d 【name】

## git 标签

-  新建一个tag: git tag 【tagname】
-  新建一个tag, 指定标签信息： git tag -a 【tagname】 -m "标签信息内容"
-  查看所有标签


## 其它
- 恢复上一个版本：git reset --hard HEAD^
> 你想回归到任何一个版本都是可以的，可以通过下面命令操作，例如想恢复到上一个版本。
![](index_files/a00c9935-742a-478d-9b1e-52f43a2ae227.png)
      在上面进行了恢复最近一个版本，可以删除的git.txt文件又回来了，是不是很方便呢，解释一下版本恢复命令： reset --hard HEAD^ ,表示上一个版本，HEAD^^,表示上两个版本，简写形式 HEAD~10表示恢复到上10个版本，这里有个问题是我们更改过很多版本但是有时候我们并不知道哪个版本改了什么东西。
      这个命令还可以用 commit_id当版本表示，如reset --hard HEAD commit_id ,
      git如果恢复到某个历史版本后，这个版本之前的状态就会查询不出来，为了还可以恢复到未来某个版本，我们需要查询最近所做的操作，可以通过git reflog 命令，得到commit_id之后再通过reset命令来达到效果，如图
![](index_files/bf2db87f-95eb-4028-8d92-c363046f12b2.png)
> 来源： http://blog.csdn.net/lilongsheng1125/article/details/49470631
