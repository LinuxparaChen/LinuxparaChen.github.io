# 这是我的私人博客

主题借鉴Papyrus. 原著作者：Hugo Sereno Ferreira. 

原著主题GitHub地址：https://github.com/mattvh/jekyllthemes


## 安装和测试

我的笔记本是Mac，所以以下步骤都是基于Mac电脑.

**以下步骤部分需要科学上网，请自备梯子.**

>###第一部分
>1. 在Github上新建一个仓库，命名为：你的账号.github.io

>2.	进入你要存放工程的目录，从我的仓库克隆一份源码：`git clone git@github.com:LinuxparaChen/LinuxparaChen.github.io.git`

>3. 更改主目录名称`mv LinuxparaChen.github.io *.github.io`*代表你的账户名称.

>4. 删除当前工程对应的远程仓库`git remote remove origin`,添加你自己的远程仓库`git remote add origin 你远程仓库的地址`.

>5. 最好垃取下你远程仓库的文件`git pull origin master`，否则你提交代码的的时候会让你先垃取远程仓库的文件.
<br>当然如果不想垃取的话也可以，使用下边这条命令，你远程仓库的文件将会丢失`git push --force origin master`.

-

>###第二部分（如果不需要在本地预览的可以忽略）
>1. 安装Homebrew(如果没有).更新brew仓库 `brew update`.

>2. 安装ruby（Mac默认版本比较2.0，需要版本2.1及以上.）查看brew仓库中ruby的版本：`brew search ruby`.
<br>安装新版ruby`brew install ruby`.
<br>安装成功后查看ruby版本：`ruby -v`，查看gem版本：`gem -v`.

>3. 安装jekyll：`sudo gem install jekyll`.

>4. 进入你的工程：`cd */*.github.io`.

>5. 安装bundle:`sudo gem install bundle`.
<br>当前工程下安装bundle：`bundle install`.

>6. 开启jekyll服务`bundle exec jekyll serve`.
<br>此时你在本地就可以预览你的个人博客，默认地址为：[http://127.0.0.1:4000](http://127.0.0.1:4000).
<br>单纯写文章我觉得这部分可依不用操作，如果是修改主题样式很需要这部分.

### 我的博客地址

- [https://linuxparachen.github.io](https://linuxparachen.github.io)

### 预览图片

![Theme preview](/assets/screenshot.png)
