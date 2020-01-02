---
title: "用hugo编写博客"
date: 2020-01-01T12:30:58+08:00
draft: false
---
# 如何用hugo编写博客
## 步骤
1. 官网下载Hugo
2. 在官网点击Quick Start
3. 在cmd中输入Quick Start的命令
   * 新建文件
```
hugo new site quickstart
```        
  
quickstart改写为github的名字（chenjinyibaby.github.io-generator），方便后续上传文件。
     
   * 增加主题 
```
git init    
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke 
echo 'theme = "ananke"' >> config.toml
```
   * 增加内容
  
    hugo new posts/my-first-post.md    

.md的名字可以随意的定义，只要是md文件就行。在这里可以写入你想输入的内容，需要将true改成false。
   * 运行在这一行你会看到一个地址，复制到浏览器就可以看到默认的效果了

    hugo server -D 

   * 定制主题（默认主题比较好用，其他的会产生bug），可以更改里面的设置。
     打开`config.toml`
   * 运行`hugo -D`（可新开一个终端运行）
运行hugo是创建了一个新的目录，目录的名字叫做public。上传到github其实就是将public上传。
  1. 将他上传到GitHub
   * `cd public`先新建一个.gitignore的文件忽略/public/。意思是当前的仓库不要储存public，我会让public自成一个仓库。
   * 运行代码
```
git init
git add .
git commit -v
```
   * 我们需要在github上新建一个仓库：chenjinyibaby.github.io(必须是这个名字)
   * 执行上传的代码，上传完后settings----master
## 如何在博客中上传新的内容
  1.  在public里面建立新的文件。追加新的内容。

    hugo new posts/xxxx.md
  2.  写完后运行重新运行 hugo
  3.  进入public，保存提交。上传