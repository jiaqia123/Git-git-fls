# GitHub上传大文件

下载 `git-lfs` 上传大文件

```cmd
git init   #创建本地仓库坏境

git lfs install  #安装大文件上传应用

git lfs track *  #追踪要上传的大文件，*表示路径下的所有文件
#git lfs track "*.zip"
#git lfs track "*.psd"
#git lfs track "*.mp4"

#.gitattributes 是 Git 的配置文件，用来告诉 Git 怎么处理特定文件（如大文件）
git add .gitattributes   #添加先上传的属性文件（要先上传属性文件，不然有可能失败）

git commit -m "Setup LFS"  #添加属性文件上传的说明

git remote add origin https://github.com/xxx.git  #建立本地和Github仓库的链接

git push origin main    #上传属性文件 
#git push -u origin main

git add *  #添加要上传的大文件，*表示路径下的所有文件

git commit -m "Git LFS commit"    #添加大文件上传的说明

git push origin main    #上传大文件
```

