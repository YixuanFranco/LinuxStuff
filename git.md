:smile:
**不知道这算不算特大喜讯**  
Mar.12 搞定了git. 其实之前貌似是学过啊。全都还给老师我也是很醉。  

###将本地文件上传到Github的方法。  
1. `git init` +**文件夹名**可在本地新建文件夹。  
2. 向文件夹中添加任意文件。  
**关键步骤**, 在终端中使用cd命令, 转到新建文件夹. 不然可能显示不出来.   
    `git status` :To see current state. You could do this often.   
> When it shows `somefile` is untracked, that means it a new file.   
3. `git add filename`:To tell git to start tracking changes made to file. Now the file is staged(which means it is about to commit.)   
4. `git commit -m "command"`:To store our staged changes we run the commit command with a message describing what we've change.   
> 所以文件首先要add（staged）, 而后要commit（注意：此时还没有上传到github）   
5. `git remote add origin ...address`:To push our local stuff to github server.   
> P.s第二次可能会显示origin already exist. ^_^其实第二次就已经不用再打这个代码啦。
6. `git push -u origin master`：下次就可以直接用**git push**了。  
> 到这一步, 就可以去刷新github了. 上面会显示你从本地上传的东西了.    


注意:明白转换分支的重要性. 如学不会merge分支. push之后会导致github的文件有两份，一个是改动前，一个是改动后。   
所以学习一些`checkout`看来也是必须的。明天继续总结。


所以在添加新内容 后，应add，commit，添加分支，删除分支，合并。push。   

因为有时候, 改动前的文章会是git.md~   
所以我们需要合并分支并且删除没用的文件。   

具体操作：   
`git branch Yixuan`    
> Here you add a new branck which is the copy of the master.    

` git checkout Yixuan`   
> Switch to the Yixuan branch   

` git rm 'filename'`   
> delete this file in Yixuan Branch   

Or you could use `git rm -r folder_of_` to delete a folder.   

` git checkout master`   
> switch back to master   

` git merge Yixuan`   
    合并   

`git branch -d Yixuan`
> You don't need this branch anymore, so you could delete it before push.

` git push`
